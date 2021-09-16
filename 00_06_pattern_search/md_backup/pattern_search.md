# 과거 주가 데이터로 미래 주가를 예측할 수 있을까? | 파이썬 패턴 검색기 구현

주가 예측은 오래 전부터 많은 사람들의 관심을 받아왔다. 주가의 오르내림은 정규분포에 매우 근사하기 때문에 예측이 불가능하다는 주장(패턴의 규칙이 없다는 뜻)도 있고 강화학습, 딥러닝이 단기간 예측을 가능하게 한다는 주장도 있다. 결국 어느 쪽이 맞을지는 모르겠지만 하락장에서도 AI 로보어드바이저가 돈을 벌었다는 기사들을 보면 숨은 보석같은 공식을 찾아내고 싶은 욕구가 생긴다.

AI까지 가지 않더라도 단타 세계에서는 이미 차트 매매법이라고 해서 과거 차트 패턴에 따라 앞으로의 주가를 예측할 수 있다는 전문가들이 많다. 그들의 유튜브 구독자 수만 봐도 얼마나 많은 사람들이 단타와 차트매매기술에 관심이 많은지 알 수 있다. 이들 세계에서는 그들만 아는 비밀의 법칙과 매매 기술들이 존재하겠지만 널리 알려진 것들도 많다. 이번에는 아쉬운대로 알려진 것들 중 **현재 차트와 유사한 차트를 찾아서 매매에 활용하는 패턴 검색**을 파이썬으로 구현해보려고 한다. 

**패턴 검색**을 하는 이유는 과거 패턴이 유사한 차트를 찾아서 다음 날짜에 주가가 올랐다면 매수하고, 내렸다면 매도하기 위해서다. 당연한 말이지만 실제로 매수할지 말지에 대한 판단은 본인의 몫이며 이에 따른 손익 역시 전적으로 본인의 책임이다.

```
목차
___
Step 1. 라이브러리 호출 및 코스피 지수 추출
Step 2. 기준 구간 지정 및 시각화
Step 3. 패턴 검색기 구현
Step 4. 검색 구간 이후의 추세 확인
```

## 1. 라이브러리 호출 및 코스피 지수 추출

주가 데이터를 가져오기 위해 FinanceDataReader라는 파이썬 오픈소스를 사용하고 matplotlib을 통해 주가 차트를 시각화할 것이다. 따라서 해당 라이브러리를 import해준다.

또한 패턴 검색을 구현하기 위해 과거 데이터와 현재 데이터를 서로 '코사인 유사도'로 비교할텐데 이를 위해 scipy 패키지의 cosine함수를 사용하겠다.


```python
import FinanceDataReader as fdr
import matplotlib.pyplot as plt

# 1차월 배열간 코사인 유사도 계산
from scipy.spatial.distance import cosine
```

다음으로 코스피지수를 추출해서 어떤 칼럼들이 있는지 데이터로 살펴보자.


```python
# 코스피 지수 추출
kospi = fdr.DataReader('KS11')
```


```python
kospi
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Close</th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Volume</th>
      <th>Change</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1981-05-01</th>
      <td>123.60</td>
      <td>123.60</td>
      <td>123.60</td>
      <td>123.60</td>
      <td>3330000.0</td>
      <td>0.0098</td>
    </tr>
    <tr>
      <th>1981-05-02</th>
      <td>123.50</td>
      <td>123.50</td>
      <td>123.50</td>
      <td>123.50</td>
      <td>2040000.0</td>
      <td>-0.0008</td>
    </tr>
    <tr>
      <th>1981-05-04</th>
      <td>120.60</td>
      <td>120.60</td>
      <td>120.60</td>
      <td>120.60</td>
      <td>1930000.0</td>
      <td>-0.0235</td>
    </tr>
    <tr>
      <th>1981-05-06</th>
      <td>120.70</td>
      <td>120.70</td>
      <td>120.70</td>
      <td>120.70</td>
      <td>1690000.0</td>
      <td>0.0008</td>
    </tr>
    <tr>
      <th>1981-05-07</th>
      <td>119.30</td>
      <td>119.30</td>
      <td>119.30</td>
      <td>119.30</td>
      <td>1480000.0</td>
      <td>-0.0116</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2021-09-10</th>
      <td>3125.76</td>
      <td>3121.09</td>
      <td>3131.54</td>
      <td>3103.38</td>
      <td>723080000.0</td>
      <td>0.0036</td>
    </tr>
    <tr>
      <th>2021-09-13</th>
      <td>3127.86</td>
      <td>3117.35</td>
      <td>3139.13</td>
      <td>3109.01</td>
      <td>732270000.0</td>
      <td>0.0007</td>
    </tr>
    <tr>
      <th>2021-09-14</th>
      <td>3148.83</td>
      <td>3137.32</td>
      <td>3164.31</td>
      <td>3137.32</td>
      <td>713230000.0</td>
      <td>0.0067</td>
    </tr>
    <tr>
      <th>2021-09-15</th>
      <td>3153.40</td>
      <td>3147.21</td>
      <td>3164.01</td>
      <td>3138.80</td>
      <td>616560000.0</td>
      <td>0.0015</td>
    </tr>
    <tr>
      <th>2021-09-16</th>
      <td>3130.09</td>
      <td>3165.38</td>
      <td>3167.68</td>
      <td>3126.65</td>
      <td>604460.0</td>
      <td>-0.0074</td>
    </tr>
  </tbody>
</table>
<p>10790 rows × 6 columns</p>
</div>



## 2. 기준 구간 지정 및 시각화

패턴 검색을 위해서는 종가만 있으면 된다. 더 복잡한 `무언가`를 구현하고자 한다면 나머지 칼럼도 활용해보길 바란다.

종가 데이터는 'Close' 칼럼에 있다. 이와 함께 현재 어느 시점의 차트를 기준으로 검색할 것인지 날짜 구간을 변수에 저장해준다.


```python
# 기준 기간 종가
kospi_close[d_start:d_end]
```




    Date
    2021-09-01    3207.02
    2021-09-02    3175.85
    2021-09-03    3201.06
    2021-09-06    3203.33
    2021-09-07    3187.42
    2021-09-08    3162.99
    2021-09-09    3114.70
    2021-09-10    3125.76
    2021-09-13    3127.86
    2021-09-14    3148.83
    2021-09-15    3153.40
    2021-09-16    3130.09
    Name: Close, dtype: float64




```python
# 종가만 추출
kospi_close = kospi['Close']

# 비교 기준 구간
d_start = '2021-09-01'
d_end = '2021-09-16'
```

기준 구간을 시각화해보자.


```python
# 기준 구간 시계열 차트
kospi_close[d_start:d_end].plot();
```


    
![png](output_14_0.png)
    


위 차트와 유사한 과거의 차트를 찾아내는 것이 이번 분석의 목적이다.

## 3. 패턴 검색기 구현

패턴 검색의 원리는 이렇다. 먼저 앞에서 지정한 기준 구간의 데이터가 있을 것이다. 해당 데이터 길이만큼 최초 상장일부터 하루씩 비교하면서 코사인 유사도를 계산한다. 단, 과거의 주가와 현재 주가의 액수 차이가 크기 때문에 `패턴`만 추출하기 위해서 표준화를 먼저 수행한 다음 데이터를 비교해야 한다. 

이렇게 모든 데이터를 비교해서 코사인 유사도가 가장 작은 값 즉, 현재 주가 패턴과 가장 유사한 과거 시점의 주가를 찾는 방식이다. 코드로 구현해보자.


```python
count = 0
compare_base_r = kospi_close[d_start:d_end]
# series에서 값만 추출
compare_base = compare_base_r.values
# 표준화
compare_base_norm = (compare_base - compare_base.mean()) / compare_base.std()
# array -> 1차원 리스트로 변환
compare_base_norm = list(compare_base_norm)

# 검색 기간
window_size = len(compare_base_norm)
# 검색 기간에 더해서 추가로 보여줄 기간
next_date = 5
# 검색 횟수
moving_cnt = len(kospi_close) - (window_size-1) - next_date

# 유사도 저장 딕셔너리
sim_dict = {}

for i in range(moving_cnt):
    compare_target_r = kospi_close[i:i+window_size]
    # series에서 값만 추출
    compare_target = compare_target_r.values
    # 표준화
    compare_target_norm = (compare_target - compare_target.mean()) / compare_target.std() 
    # array -> 1차원 리스트로 변환
    compare_target_norm = list(compare_target_norm)

    # 코사인 유사도 저장
    sim = cosine(compare_base_norm, compare_target_norm)
    # 코사인 유사도 <- i(인덱스), 시계열데이터 함께 저장
    sim_dict[sim] = [i,compare_target_r]
```

이렇게 반복문을 통해 모든 코사인 유사도를 단일 리스트에 저장했다면, 이 값이 가장 작았던 구간을 추출해야 한다. 다행히 우리는 반복문에서 인덱스를 함께 저장했기 때문에 간단하게 불러낼 수 있다.


```python
# 최소 코사인 유사도
min_sim = min(list(sim_dict.keys()))
# 최소 코사인 유사도가 나온 인덱스, 기간 추출
sim_dict[min_sim]
```




    [2689,
     Date
     1990-07-06    716.17
     1990-07-07    713.41
     1990-07-09    715.28
     1990-07-10    718.75
     1990-07-11    711.00
     1990-07-12    701.91
     1990-07-13    688.78
     1990-07-14    689.19
     1990-07-16    683.01
     1990-07-18    698.01
     1990-07-19    693.44
     1990-07-20    694.64
     Name: Close, dtype: float64]



그래서 이때의 주가 패턴이 얼마나 현재 패턴과 유사한지 궁금할 것이다. 두 그래프를 동시에 그려보자. 단, 주 시점의 주가 차이를 상쇄하기 위해 앞에서 유사도를 계산할 때 표준화를 했던 것처럼 이번에도 역시 표준화를 진행하고 그래프를 그릴 것이다.


```python
# 표준화된 기준 구간 데이터 
compare_base_norm
```




    [1.4339539201757012,
     0.45149073936036144,
     1.2460976302283338,
     1.3176469218693603,
     0.8161714901474522,
     0.04614981843365735,
     -1.4759274033043155,
     -1.1273216035026465,
     -1.0611306288567652,
     -0.400166467750014,
     -0.25612229911587053,
     -0.9908421176851828]




```python
# 검색 구간 데이터 -> 값만 추출
compare_target = compare_target_r.values
# 검색 구간 데이터 표준화
compare_target_norm = (compare_target - compare_target.mean())/compare_target.std()
compare_target_norm = list(compare_target_norm)

# 표준화된 검색 구간 데이터
compare_target_norm
```




    [1.1892892589786803,
     0.9581994364068187,
     1.1147711640189142,
     1.4053080061654246,
     0.7564144826393618,
     -0.004674824309274292,
     -1.1040260454573,
     -1.06969748485785,
     -1.5871377397470252,
     -0.33121479098690393,
     -0.7138526493758155,
     -0.6133788134750116]




```python
plt.plot(compare_base_norm, label='base')
plt.plot(compare_target_norm, label='target')
plt.legend()
plt.show()
```


    
![png](output_24_0.png)
    


두 그래프의 추세가 매우 유사하다. 복잡한 코드 없이 몇 줄 안되는 간단한 코드로 구현한 패턴 검색기임에도 나름대로 제 역할을 잘 하는 것 같다.

## 4. 검색 구간 이후의 추세 확인

이번에는 해당 구간 이후 주가가 어떻게 움직였는지 볼 것이다. 우리가 궁금한 것은 '앞으로의 주가가 어떻게 될 것인가?'이기 때문이다.


```python
# 반복문 인덱스 복원
idx = sim_dict[min_sim][0]
# 반복문 타겟 구간 시계열 데이터 복원
compare_target_r = sim_dict[min_sim][1]

plt.figure(figsize=(12,4))
expanded_target_r = kospi_close[idx:idx+window_size+next_date]
expanded_target_r.plot()
plt.axvspan(compare_target_r.index[-1], expanded_target_r.index[-1], facecolor='gray', alpha=0.5)
plt.axvline(x=compare_target_r.index[-1], c='r', linestyle='--')
plt.xticks(rotation=90)
plt.show()
```


    
![png](output_28_0.png)
    


현재 패턴과 유사한 과거 패턴을 찾았고, 해당 패턴을 보인 과거의 특정 구간 이후에는 약 5일간 주가가 하락했다. 

오늘이 9월 16일이니 앞으로 5일간 주가를 감상해보면 **패턴 검색이 과연 미래를 예측할 수 있는가**에 대해 검증할 수 있다. 물론 재미로만 보자.
