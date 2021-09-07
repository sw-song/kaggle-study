> \* 티스토리 마크다운이 최적화되어 있지 않습니다. 동일한 본문을 [깃허브 블로그](https://sw-song.github.io/data%20collection/pykiwoom/)에도 올려두었으니 참고부탁드립니다.

[##_Image|kage@zrHdy/btrdQA2Mol8/YdZOCF8PuzQsZzMOfxwBPk/img.png|alignLeft|data-origin-width="796" data-origin-height="264" data-filename="스크린샷 2021-09-02 오후 9.17.14.png" width="627" data-ke-mobilestyle="widthOrigin"|||_##]

# 키움 증권 API를 활용한 주식 정보 및 일봉 데이터 수집 자동화

-   pykiwoom 모듈 활용 : [github/sharebook-kr/pykiwoom](https://github.com/sharebook-kr/pykiwoom)
-   코드 참고 : [퀀트투자를 위한 키움증권 API, 조대표 외 1명](https://wikidocs.net/book/1173)

## 1\. 개요

### 1-1. 주식 데이터 수집 방식 비교

주가 정보를 수집하기 위한 방법으로는 주로 금융사에서 제공하는 api방식과 웹스크래핑 방식이 있다.

금융사 api를 활용하면 주가 정보 외에도 일반적으로 주식앱에서 볼 수 있는 다양한 데이터를 불러올 수 있다.

또한, api에서는 실시간 데이터 조회 기능도 제공하기 때문에 매매자동화 등에 활용할 수 있다.

### 1-2. pykiwoom

일반적으로 파이썬으로 키움 api를 사용하는 경우 Python GUI 패키지인 PyQt5를 활용하게 된다.

그러나 실시간 시세 정보를 활용해 매매자동화 프로그램을 구현하는 경우가 아니라면 다른 사용자들이 미리 raw 코드를 wrapping 해놓은 코드, 즉 PyQt5 등으로 구현한 코드를 클래스 및 함수로 한번 감싸서 더 단순하게 사용할 수 있도록 한 코드를 이용해보는 것도 좋은 방법이다.

여기서는 [파이썬으로 배우는 알고리즘 트레이딩](https://wikidocs.net/book/110) 저자로 유명한 `조대표`님이 구현해주신 오픈소스 pykiwoom 패키지를 사용한다.

## 2\. 로그인 및 접속 상태 조회

### 2-1. 환경 설정

본격적으로 코드 실습 전, 필요한 환경을 반드시 세팅해야 한다.

-   window 10 이상(권장)
-   python 3.7 이상(32bit 필수\*)
-   키움증권 개좌 개설 및 API 사용 신청(필수)
-   키움증권 Open API+ 모듈 설치(필수)
-   KOA Studio 설치(필수, 데이터 조회 키 및 자동로그인 설정용)

python의 경우 대부분은 이미 64bit로 설치되어 있을 것이다. 만약 아나콘다가 설치되어있다면 간단히 32bit 가상환경을 새롭게 세팅해주면 된다. 쉘 명령어는 아래와 같다.

```
set CONDA_FORCE_32BIT=1
conda create -n py37_32 python=3.7 anaconda
```

### 2-2. 자동 로그인 실행

아래 코드는 자동 로그인 후 로그인 정보를 돌려준다.

단, 자동 로그인을 가능하게 하기 위해서는 미리 KOA Studio에서 OpenAPI를 연결 후 윈도우 하단 상태바에 생긴 OpenAPI+ 아이콘을 우클릭하여 '계좌비밀번호 저장'을 선택하고, 비밀번호는 0000, AUTO를 체크하여 자동로그인이 가능하도록 설정한다.

```
from pykiwoom.kiwoom import *
import time
import pandas as pd

# login
kiwoom = Kiwoom() # allocation
print('login..')
kiwoom.CommConnect(block=True) # waiting to login
print('login..complete')

# connect
state = kiwoom.GetConnectState()
if state == 0:
    print('not connected')
elif state == 1:
    print('status : connected')

# login - information
account_num = kiwoom.GetLoginInfo('ACCOUNT_CNT') # number of account
accounts = kiwoom.GetLoginInfo('ACCNO') # list of account
user_id = kiwoom.GetLoginInfo('USER_ID') # user id
user_name = kiwoom.GetLoginInfo('USER_NAME') # user name
print('number of account : {}'.format(account_num))
#print('acounts : {}'.format(accounts))
#print('user id : {}'.format(user_id)) 
#print('user name : {}'.format(user_name))
```

```
login..
login..complete
status : connected
number of account : 2
```

## 3\. 기본 종목 정보 수집

### 3-1. 종목 코드 수집

아래 코드를 실행하면 코스피, 코스닥, ETF에 포함된 모든 종목 코드를 불러올 수 있다.

수집된 종목 코드를 활용하면 코스피 전체 데이터를 가져오는 등 리스트 형태로 유용하게 활용할 수 있다.

```
# kospi  : 0
# kosdaq : 10
# etf    : 8
code_kospi = kiwoom.GetCodeListByMarket('0') 
code_kosdaq = kiwoom.GetCodeListByMarket('10') 
code_etf = kiwoom.GetCodeListByMarket('8') 

print('number of kospi code : {}'.format(len(code_kospi)))
print('number of kosdaq code : {}'.format(len(code_kosdaq)))
print('number of etf code : {}'.format(len(code_etf)))
```

```
number of kospi code : 1634
number of kosdaq code : 1511
number of etf code : 500
```

### 3-2. 개별 종목 정보 수집

pykiwoom 패키지를 통해 간편하게 기업명, 전일가 등을 불러올 수 있다.

아래 코드는 기본적인 종목 정보를 불러온다.

```
# 카카오 : 035720
corp = kiwoom.GetMasterCodeName('035720')
con = kiwoom.GetMasterConstruction('035720')
listed_d = kiwoom.GetMasterListedStockDate('035720')
prev_price = kiwoom.GetMasterLastPrice('035720')
state = kiwoom.GetMasterStockState('035720')

print('기업 : {}'.format(corp))
print('감리구분 : {}'.format(con))
print('최초상장일 : {}'.format(listed_d))
print('전일가 : {}'.format(prev_price))
print('종목상태 : {}'.format(state))

```

```
기업 : 카카오
감리구분 : 정상
최초상장일 : 2017-07-10 00:00:00
전일가 : 148500
종목상태 : ['증거금20%', '담보대출', '신용가능']
```

> 여기서 '최초상장일'은 카카오가 현재 상장된 시장인 '코스피'에 최초로 상장된 날짜를 뜻한다.

## 4\. 주가 정보 수집

### 4-1. 개별 주식 정보 수집

특정 종목코드에 해당하는 주식 정보를 불러오고 싶다면 'opt10001'를 호출한다.

'opt10001'은 가장 기본적인 주식 정보를 반환하는 TR key다. TR이란 api를 통해 요청하는 transaction을 의미하며, 딕셔너리 형태로 구성되어 있기 때문에 'opt10001'이라는 key를 입력값으로 전달하면 된다. KOA Studio를 통해 이 외에도 다양하고 유용한 TR을 살펴볼 수 있다.

```
# opt10001 : (TR)주식기본정보요청
# single data (has single row)
df_single = kiwoom.block_request('opt10001',
                          종목코드='035720',
                          output='주식기본정보',
                          next=0 # 0 : single transaction
                          )

# 출력
df_single
```

|   | 종목코드 | 종목명 | 결산월 | 액면가 | 자본금 | 상장주식 | 신용비율 | 연중최고 | 연중최저 | 시가총액 | ... | 250최저가대비율 | 현재가 | 대비기호 | 전일대비 | 등락율 | 거래량 | 거래대비 | 액면가단위 | 유통주식 | 유통비율 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 035720 | 카카오 | 12 | 100 | 445 | 444707 | +0.49 | +561000 | \-108000 | 662614 | ... | +37.96 | +149000 | 2 | +500 | +0.34 | 2017066 | \-75.31 | 원 | 324274 | 73.0 |

1 rows × 45 columns

```
df_single.T
```

|   | 0 |
| --- | --- |
| 종목코드 | 035720 |
| 종목명 | 카카오 |
| 결산월 | 12 |
| 액면가 | 100 |
| 자본금 | 445 |
| 상장주식 | 444707 |
| 신용비율 | +0.49 |
| 연중최고 | +561000 |
| 연중최저 | \-108000 |
| 시가총액 | 662614 |
| 시가총액비중 |   |
| 외인소진률 | +31.95 |
| 대용가 | 112860 |
| PER | 422.20 |
| EPS | 353 |
| ROE | 2.7 |
| PBR | 10.47 |
| EV | 87.91 |
| BPS | 14237 |
| 매출액 | 41568 |
| 영업이익 | 4559 |
| 당기순이익 | 1734 |
| 250최고 | +561000 |
| 250최저 | \-108000 |
| 시가 | +150000 |
| 고가 | +150500 |
| 저가 | \-148000 |
| 상한가 | +193000 |
| 하한가 | \-104000 |
| 기준가 | 148500 |
| 예상체결가 | +149500 |
| 예상체결수량 | 1203 |
| 250최고가일 | 20210408 |
| 250최고가대비율 | \-73.44 |
| 250최저가일 | 20210513 |
| 250최저가대비율 | +37.96 |
| 현재가 | +149000 |
| 대비기호 | 2 |
| 전일대비 | +500 |
| 등락율 | +0.34 |
| 거래량 | 2017066 |
| 거래대비 | \-75.31 |
| 액면가단위 | 원 |
| 유통주식 | 324274 |
| 유통비율 | 73.0 |

### 4-2. 개별 주식 일봉 차트 조회

일명 캔들이라 불리는 일봉 차트를 조회하는 방법은 아래와 같다.

일봉차트 정보는 매일 거래된 정보에 대해 시가,고가,저가,현재가(종가)를 담고 있으며 일반적으로 투자자들이 주가 추세를 확인할 때 보는 가장 기본적인 데이터다.

```
# opt10081 : (TR)주식일봉차트조회요청
# multi-data (has multiple rows)
df_multi = kiwoom.block_request('opt10081',
                          종목코드='035720',
                          기준일자='20210824', # 기준일로부터 총 600일(변동가능)
                          수정주가구분=1, # 수정주가 적용(액분 등 반영)
                          output='주식일봉차트조회', # multi-data
                          next=0 # 0 : single transaction(단일 요청)
                          )

# 기준일자 '2021년 8월 24일' 포함 지난 600일 일봉 데이터 출력
df_multi

```

|   | 종목코드 | 현재가 | 거래량 | 거래대금 | 일자 | 시가 | 고가 | 저가 | 수정주가구분 | 수정비율 | 대업종구분 | 소업종구분 | 종목정보 | 수정주가이벤트 | 전일종가 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 035720 | 149000 | 2017066 | 300363 | 20210824 | 150000 | 150500 | 148000 |   |   |   |   |   |   |   |
| 1 |   | 148500 | 2678395 | 393910 | 20210823 | 146000 | 148500 | 144500 |   |   |   |   |   |   |   |
| 2 |   | 144000 | 2776813 | 403451 | 20210820 | 146500 | 149000 | 143000 |   |   |   |   |   |   |   |
| 3 |   | 146500 | 2813914 | 412982 | 20210819 | 144000 | 149000 | 144000 |   |   |   |   |   |   |   |
| 4 |   | 145500 | 2720552 | 392335 | 20210818 | 142000 | 146500 | 141500 |   |   |   |   |   |   |   |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |
| 595 |   | 20672 | 1076891 | 22260 | 20190401 | 20772 | 20873 | 20471 |   |   |   |   |   |   |   |
| 596 |   | 20772 | 766432 | 15861 | 20190329 | 20672 | 20873 | 20572 |   |   |   |   |   |   |   |
| 597 |   | 20572 | 811988 | 16766 | 20190328 | 20471 | 20873 | 20471 |   |   |   |   |   |   |   |
| 598 |   | 20572 | 1039895 | 21532 | 20190327 | 20973 | 20973 | 20471 |   |   |   |   |   |   |   |
| 599 |   | 20873 | 1282770 | 26846 | 20190326 | 20572 | 21174 | 20471 |   |   |   |   |   |   |   |

600 rows × 15 columns

키움 API는 기본적으로 일봉차트조회시 총 600줄(600일)에 해당하는 정보를 돌려준다.

따라서 600일이 넘는 일별 거래 정보가 필요한 경우 반복문을 통해 코딩을 해줘야 한다.

pykiwoom 패키지를 사용하는 경우 `tr_remained` 모듈로 아래와 같이 연속 조회가 가능하다.

```
# opt10081 : (TR)주식일봉차트조회요청
# multi-data (has multiple rows)
# 연속 조회 방식 (while kiwoom.tr_record)

tr = "opt10081"
code = "035720"
set_d = '20210824'

df_list = []
df_firstblock = kiwoom.block_request(tr,
                          종목코드=code,
                          기준일자=set_d,
                          수정주가구분=1,
                          output="주식일봉차트조회",
                          next=0)
df_list.append(df_firstblock)
print('데이터 수집 시작.. ({}~)'.format(df_firstblock.loc[0,'일자']))
print('데이터 수집 중.. (~{})'.format(df_firstblock.loc[len(df_firstblock)-1,'일자']))

# 남은 데이터가 있다면 실행
while kiwoom.tr_remained:
    df_remainblock = kiwoom.block_request(tr,
                              종목코드=code,
                              기준일자=set_d,
                              수정주가구분=1,
                              output="주식일봉차트조회",
                              next=2)
    df_list.append(df_remainblock)
    time.sleep(1)
    print('데이터 수집 중.. (~{})'.format(df_remainblock.loc[len(df_remainblock)-1,'일자']))
    if kiwoom.tr_remained == False:
        print('데이터 수집 완료')

df_all = pd.concat(df_list)
df_all.reset_index(drop=True, inplace=True)
```

```
데이터 수집 시작.. (20210824~)
데이터 수집 중.. (~20190326)
데이터 수집 중.. (~20161011)
데이터 수집 중.. (~20140429)
데이터 수집 중.. (~20111128)
데이터 수집 중.. (~20090707)
데이터 수집 중.. (~20070201)
데이터 수집 중.. (~20040903)
데이터 수집 중.. (~20020329)
데이터 수집 중.. (~19991111)
데이터 수집 완료
```

```
df_all
```

|   | 종목코드 | 현재가 | 거래량 | 거래대금 | 일자 | 시가 | 고가 | 저가 | 수정주가구분 | 수정비율 | 대업종구분 | 소업종구분 | 종목정보 | 수정주가이벤트 | 전일종가 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 035720 | 149000 | 2017066 | 300363 | 20210824 | 150000 | 150500 | 148000 |   |   |   |   |   |   |   |
| 1 |   | 148500 | 2678395 | 393910 | 20210823 | 146000 | 148500 | 144500 |   |   |   |   |   |   |   |
| 2 |   | 144000 | 2776813 | 403451 | 20210820 | 146500 | 149000 | 143000 |   |   |   |   |   |   |   |
| 3 |   | 146500 | 2813914 | 412982 | 20210819 | 144000 | 149000 | 144000 |   |   |   |   |   |   |   |
| 4 |   | 145500 | 2720552 | 392335 | 20210818 | 142000 | 146500 | 141500 |   |   |   |   |   |   |   |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |
| 5374 |   | 1654 | 2021 | 3 | 19991117 | 1654 | 1654 | 1654 |   |   |   |   |   |   |   |
| 5375 |   | 1479 | 2265 | 3 | 19991116 | 1479 | 1479 | 1479 |   |   |   |   |   |   |   |
| 5376 |   | 1323 | 4286 | 6 | 19991115 | 1323 | 1323 | 1323 |   |   |   |   |   |   |   |
| 5377 |   | 1181 | 1481 | 2 | 19991112 | 1181 | 1181 | 1181 |   |   |   |   |   |   |   |
| 5378 |   | 1058 | 127 | 0 | 19991111 | 1058 | 1058 | 1058 |   |   |   |   |   |   |   |

5379 rows × 15 columns

여기까지 pykiwoom 패키지를 활용해 키움 openapi에 자동으로 로그인하여 가장 기본적인 종목 정보와 개별 주가 데이터를 수집해보았다.

그러나 이러한 작업은 단순히 데이터를 수집하는 목적이라면 큰 의미가 없고, 불필요하다. 증권사 앱 혹은 네이버 검색만으로 주가정보는 너무나 편리하게 확인할 수 있기 때문이다.

심지어 자체 DB를 구축한다 하더라도 일자별 거래데이터의 경우 yahoofinance와 같은 더 편리한 파이썬 패키지가 있기 때문에 굳이 금융사 api로 접근해서 데이터를 불러오지 않아도 된다.

만약, 개인 투자 자동화 및 모의투자 매매 실험을 위한 프로그래밍이라면 금융사 api는 사실상 유일한, 가장 최선의 도구다.