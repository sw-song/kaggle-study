```
구성:

# TIA(Today I Analyzed) - My Project
## Description
가설 검정을 통한 데이터 분석 뿐만 아니라 웹 스크래핑이나 API를 사용한 데이터 수집, 머신러닝 예측 모델링 등 
다양한 프로젝트를 통해 데이터 활용 및 분석 스킬을 업데이트하고 있습니다.
- 폴더명이 00_로 시작합니다.
- (참고)8번 프로젝트부터 본 레포지토리를 코드 저장소로 활용합니다. 
분석 내용과 자세한 설명은 블로그에 기록하고 있으니 하단에서 각 프로젝트 링크를 참고바랍니다.

# TIA(Today I Analyzed) - Kaggle Study
## Description
좋은 커널이 있다면 따라 작성하면서 공부해보고, 직접 분석도 하고 있습니다. 
따라 작성한 코드의 경우 Readme 목차 타이틀에 +표시를 해뒀습니다.
- 타이틀 번호는 데이터에 따라 매겼습니다. 
- 번호가 같다면 동일한 데이터를 사용한 코드입니다.
- 번호가 없다면(ex. 20) 직접 분석한 커널이 없는 경우입니다.
```


# TIA(Today I Analyzed) - My Project
## Description
가설 검정을 통한 데이터 분석 뿐만 아니라 웹 스크래핑이나 API를 사용한 데이터 수집, 머신러닝 예측 모델링 등 
다양한 프로젝트를 통해 데이터 활용 및 분석 스킬을 업데이트하고 있습니다.

**[1. 넷플릭스의 콘텐츠 보유 현황과 수급 전략 분석](https://github.com/sw-song/TIA/blob/main/00_01_netflix_trend_analysis/analysis_strategy_in_netflix.ipynb)**
```
Step 1. 가설 설정
Step 2. 기본 전처리
     2-1. 불필요한 컬럼 제거
     2-2. 불필요한 행 제거
     2-3. 데이터 타입 변환
     2-4. 시계열 데이터 변환
     2-5. 데이터 구간(시간) 분할
Step 3. 가설 검정
     3-1. 특정 콘텐츠 유형에 대한 집중 수급 여부 분석
     3-2. 특정 국가를 겨냥한 콘텐츠 현황 분석
     3-3. 콘텐츠 수급 대상 연도 분석
     3-4. 넷플릭스의 주요 소비자 타겟(연령대) 분석
     3-5. 콘텐츠 평균 재생 시간 분석
     3-5. 넷플릭스에서 주로 수급하는 콘텐츠 장르 분석
Step 4. 종합 결론
```

**[2. 커머스 고객의 연간 지출액 분석을 통한 매출 개선 시뮬레이션](https://github.com/sw-song/TIA/blob/main/00_02_ecommerce/ecommerce.ipynb)**
```
Step 1. 가설 설정
Step 2. 가설 검정
     2-1. 평균 세션 접속 시간에 따른 연간 지출액 확인
     2-2. 가입 기간에 따른 연간 지출액 확인
     2-3. 앱, 웹 사용 시간 비교
     2-4. 앱 사용 시간에 따른 연간 지출액 확인
     2-5 웹 사용 시간에 따른 연간 지출액 확인
     2-6. 가입 기간에 따른 구매 경로에 대한 선호도 차이 분석
     2-7. 가입 기간에 따른 구매 경로 별 연간 지출액 확인
Step 3. 분석 결과
Step 4. 매출 개선 시뮬레이션
```

**[3. 증권사(키움증권) API를 활용한 비 실시간(Batch) 주가 정보 수집](https://github.com/sw-song/TIA/blob/main/00_03_pykiwoom/pykiwoom_test.ipynb)**
```
Step 1. 개요
     1-1. 주식 데이터 수집 방식 비교
     1-2. pykiwoom
Step 2. 로그인 및 접속 상태 조회
     2-1. 환경 설정
     2-2. 자동 로그인 실행
Step 3. 기본 종목 정보 수집
     3-1. 종목 코드 수집
     3-2. 개별 종목 정보 수집
Step 4. 주가 정보 수집
     4-1. 개별 주식 정보 수집
     4-2. 개별 주식 일봉 차트 조회
```

**[4. 가설 검정을 통한 카카오 주식 매매 백테스팅](https://github.com/sw-song/TIA/blob/main/00_04_backtesting/kakao_backtesting.ipynb)**
```
Step 1. 카카오 주식을 1999년 11월 11일에 100만원 치 샀다면 오늘 얼마일까?
     1-1. 라이브러리 호출 및 데이터 확인
     1-2. 가설 검정
Step 2. 카카오 주가는 언제나 상승장이었을까?
     2-1. 가설 검정(일봉 차트)
     2-2. 가설 검정(365일 이동평균선)
Step 3. 수면제 먹고 자는 것보다 더 나은 수익을 낼 수 있을까?
     3-1. 이동 평균 데이터 추가
     3-2. 데이터 전처리(change 컬럼)
     3-3. 백테스팅 전략 설계
     3-4. 데이터 전처리(매매 구간 처리 - overs 컬럼)
     3-5. 데이터 전처리(매매 신호 표기 - signal 컬럼)
     3-6. 가설 검정(매입액 현재가 비교)
```

**[5. (1) 문제 상황 가정 및 데이터 전처리 | 광고 프로모션 효율 증진을 위한 커머스 고객 세분화](https://github.com/sw-song/TIA/blob/main/00_05_customer_segmentation/customer_personality_analysis.ipynb)**
```
Step 1. 문제 상황 가정 및 데이터 전처리 
     1-1. 라이브러리 호출 및 데이터 확인 
     1-2. 일부 컬럼 제거 
     1-3. 컬럼명, 데이터타입 형식 통일 
     1-4. 현재 날짜 가정 
     1-5. 이상치 처리
```

**[5. (2) 고객 군집 분석 | 광고 프로모션 효율 증진을 위한 커머스 고객 세분화](https://github.com/sw-song/TIA/blob/main/00_05_customer_segmentation/customer_personality_analysis.ipynb)**
```
Step 2. 고객 그룹 세분화
     2-1. 나이에 따라 분류하기
     2-2. 최근 구매일자에 따라 분류하기
     2-3. 가입 기간에 따라 분류하기
     2-4. 컴플레인 여부에 따라 분류하기
     2-5. 온/오프라인 선호도에 따라 분류하기
     2-6. 프로모션 동의 여부에 따라 분류하기
     2-7. 머신러닝으로 분류하기
```

**[6. 과거 주가 데이터로 미래 주가를 예측할 수 있을까? | 파이썬 패턴 검색기 구현](https://github.com/sw-song/TIA/blob/main/00_06_pattern_search/pattern_search.ipynb)**
```
Step 1. 라이브러리 호출 및 코스피 지수 추출
Step 2. 기준 구간 지정 및 시각화
Step 3. 패턴 검색기 구현
Step 4. 검색 구간 이후의 추세 확인
```

**[7. AI, 딥러닝으로 주가를 예측할 수 있다고?](https://github.com/sw-song/TIA/blob/main/00_07_price_forecasting/linear_reg.ipynb)**
```
Step 1. 시계열 데이터와 예측
Step 2. 예측 실험
Step 3. 결과 해석
```

**[8. (코드)Bitcoin price forecasting](https://github.com/sw-song/TIA/blob/main/00_08_holt_winters/bitcoin_predict.ipynb)**
- [(설명)데이터로 보는 비트코인 가격 전망 - 이동평균부터 지수평활까지](https://songseungwon.tistory.com/entry/데이터로-보는-비트코인-가격-전망-이동평균부터-지수평활까지)


# TIA(Today I Analyzed) - Kaggle Study
## Description
좋은 커널이 있다면 따라 작성하면서 공부해보고, 직접 분석도 하고 있습니다. 
따라 작성한 코드의 경우 타이틀에 +표시를 해뒀습니다.
* **Self** : n. Main Title
* **Clone** : n+. Main Title - Clone Project(Original Title)

---
**[1. HR Analytics : Job Change of Data Scientists - Predict who will move to a new job](https://github.com/sw-song/TIA/blob/main/01_HR_Analytics/HR_Analytics.ipynb)**
```
Step 1. Library Import
Step 2. Data Read
Step 3. EDA
Step 3-1. EDA - Visualization | Numerical Columns
Step 3-2. EDA - Visualization | Categorical Columns
Step 4. Train & Validation Set 분리
Step 5. Model 생성 및 학습
Step 6. Validation data Accuracy 측정
```

**[1+. HR Analytics : Job Change of Data Scientists - Clone Project(Kaggle, HR Analytics for begineer - S P Rakshith)](https://github.com/sw-song/TIA/blob/main/01_HR_Analytics/Clone__HR_Analytics_for_beginners.ipynb)**
```
Step 1. Importing the necessery libraries
Step 2. Importing the Data, head(), info()
Step 3. Checking the total number of Null Data - insa()
Step 4. Visualize the Categorical Data
Step 5. Modeling & Prediction
Step 6. Evaluation - Confusion Matrix
```

**[1+. HR Analytics : Job Change of Data Scientists - Clone Project(Kaggle, Predict who will move to a new job - Siti Khotijah)](https://github.com/sw-song/TIA/blob/main/01_HR_Analytics/Clone__Predict_who_will_move_to_a_new_job.ipynb)**
```
Step 1. Import data
Step 2. Visualization
Step 3. Check missing Value and Replace Them with average of columns
Step 4. Type Tansfer - Categorical to Numerical
Step 5. Modeling & Prediction
Step 6. Evaluation - AUC
```
---

**[2. Youtube trend Analysis : Check Daily statistics for trending Youtube videos](https://github.com/sw-song/TIA/blob/main/02_Youtube_trend_Analysis/youtube_trend_analysis.ipynb)**
```
Step 1. Data Load & EDA
Step 2. Correlation Check - Heatmap
(+Time Series)
Step 3. Visualization - Numerical Columns
Step 4. Visualization - WordCloud
Step 5. Machine Learning Modeling(Keras)
```
---
**[3. NLP with Disaster Tweets - Basic NLP Model, Score : 0.775](https://github.com/sw-song/TIA/blob/main/03_NLP_with_Disaster_Tweets/nlp_disaster_tweets.ipynb)**
```
Step 1. Library Import & Data Load
Step 2. Data Preprocessing
     2-a. Drop Columns
     2-b. Tokenizer
     2-c. Pad Sequences
     2-d. Match Data type to numpy.ndarray
Step 3. Modeling
Step 4. Model Compile
Step 5. Callbacks
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Reload Model
Step 9. Predict Test Data
```

**[3+. NLP with Disaster Tweets - Clone Project(Kaggle, NLP Getting Started Tutorial, Phill Culliton)](https://github.com/sw-song/TIA/blob/main/03_NLP_with_Disaster_Tweets/Clone_NLP_Getting_Started_Tutorial.ipynb)**
```
Step 1. Data Load & EDA
Step 2. Text -> Vectorization(One Hot Encoding)
Step 3. Cross Validation Check
Step 4. Modeling
Step 5. Save / Submission(kaggle)
```

**[3+. NLP with Disaster Tweets - Clone Project(Getting Started with Transfer Learning Using Tensorflow Hub)](https://github.com/sw-song/TIA/blob/main/03_NLP_with_Disaster_Tweets/Clone_TL_using_TFHub.ipynb)**
```
Step 0. Importing Libraries
Step 1. Loading Data
Step 2. Basic EDA
     2-a. Missing Values
     2-b. The Dependent Variable - target
     2-c. Independent Variables
Step 3. Text Preprocessing
     3-a. Text Cleaning
     3-b. Removing Stopwords
     3-c. Lemmatization
Step 4. Wordcloud
Step 5. Modeling Using Pretrained Model
     5-a. Creating Training & Testing Set
Step 6. Prediction
Step 7. Prepare for Submission
```
---

**[4. Telecom Users Dataset Analysis - Predict User's Next Action with Logistic Regression](https://github.com/sw-song/TIA/blob/main/04_Telecom_users_analysis/quick-start-eda-to-machine-learning-logistic.ipynb)**
```
Step 1. Data Load & EDA
Step 2. Data Preprocessing
Step 3. Dataset Split(Train : Test = 0.8 : 0.2)
Step 4. Modeling : Logistic Regression
```

**[4+. Telecom Users Dataset Analysis - Clone Project(Kaggle, EDA and Building models for predicting outflow](https://github.com/sw-song/TIA/blob/main/04_Telecom_users_analysis/Clone_EDA_and_Building_models_for_predicting_outflow.ipynb)**
```
Step 1. Data Description
Step 2. Dependency research and formulation of hypothesis
Step 3. Building models to predict outflow
```
---

**[5. Heart Attack Analysis and Prediction - Binary Classification with Logistic Regression](https://github.com/sw-song/TIA/blob/main/05_Heart_Attack_Analysis_and_Prediction/quick-start-Binary_Classification_with_Logistic_Regression.ipynb)**
```
Step 1. Data Description
Step 2. EDA
Step 3. Correlation Check
Step 4. Test Data Split and Standard Scaling (Test size = 0.3)
Step 5. Modeling and Prediction
```

**[5+. Heart Attack Analysis and Prediction - Clone Project(Kaggle, Heart Attack Prediction_95.4% accuracy)](https://github.com/sw-song/TIA/blob/main/05_Heart_Attack_Analysis_and_Prediction/Clone_Heart_attack_prediction.ipynb)**
```
Step 1. Data Description - missingno
Step 2. EDA - pandas_profiling
Step 3. Data preprocessing - remove Outlier, upsampling
Step 4. modeling / prediction / evaluation
Step 5. check feature importance
```
---

**[6. Bankruptcy Prediction with KNN - Acc 97%](https://github.com/sw-song/TIA/blob/main/06_Company_Bankruptcy_Prediction/Bankruptcy_Prediction_with_KNN.ipynb)**
```
Step 1. Data Description
Step 2. Data Preprocessing - MinMaxScaling
Step 3. Machine Learning Modeling & Prediction
```

**[6+. Bankruptcy_Prediction - Clone Project(Simple, yet, Powerful Bankrupt Prediction Model)](https://github.com/sw-song/TIA/blob/main/06_Company_Bankruptcy_Prediction/Clone_Powerful_Bankrupt_Prediction.ipynb)**
```
Step 1. Data Loading and Data Cleaning
Step 2. Model Based Feature Selection
Step 3. Descriptive Analysis
Step 4. Data Analysis
Step 5. Predicting bankruptcy
Step 6. Conclusions
```
---
**[7. Anomaly Detection with XGB Classifier(base model Accuracy 79%) - Facebook Recruiting IV: Human or Robot?](https://github.com/sw-song/TIA/blob/main/07_Classification_Human_or_Robot/Anomaly_Detection_with_XGBClassifier.ipynb)**
```
Step 1. Data load & EDA
Step 2. Preprocessing - replace all values with count number
Step 3. Preprocessing - Upsampling
Step 4. Train / Valid Set Split
Step 5. Modeling
Step 6. Prediction
```

---
**[8. Stroke Prediction with EASY Ensemble - Acc 90%(Random Forest Base model - 90%, Gradient Boosting Tuning Model)](https://github.com/sw-song/TIA/blob/main/08_Stroke_Prediction/stroke_prediction.ipynb)**
```
Step 1. Data Load & EDA
Step 2. Feature Engineering
     2-a. Binary Features
     2-b. Continuous Features
     2-c. Categorical Features
Step 3. Train / Test set Split & Upsampling
Step 4. Modeling & Prediction
```

**[8+. Stroke Prediction - Clone Project(Stroke Prediction Beginner's Guide)](https://github.com/sw-song/TIA/blob/main/08_Stroke_Prediction/Clone_stroke_prediction.ipynb)**
```
Step 1. Importing the necessary libraries
Step 2. Importing the Data using Pandas read_csv(). And calling head() and info() on the DataFrame
Step 3. Preprocessing Data before Exploratory Data Analysis
Step 4. Exploratory Data Analysis on Stroke Prediction Data
Step 5. Preparing the Data for Prediction
Step 6. Creating a Model for Stroke Prediction
```

---
**[9. Predict Students Performance with MultiOutputRegressor - R2(training set) 45%](https://github.com/sw-song/TIA/blob/main/09_Students_Performance_in_Exams/Predict_Students_Performance.ipynb)**
```
Step 1. Data Load & EDA
Step 2. Visualization
     2-a. Each X's distribution
     2-b. Each y's distribution
     2-c. 'X & y's distribution
Step 3. Data Preprocessing
Step 4. Modeling & Prediction
```

**[9+. Students Performance in Exams - Clone Project(Data Science Notes 4: Machine Learning(ML))](https://github.com/sw-song/TIA/blob/main/09_Students_Performance_in_Exams/Clone_Data_Science_Notes_4.ipynb)**
```
Step 1. Imports and Datasets
Step 2. Regression
     2-a. Linear Regression 
     2-b. Decision Tree Regressor
     2-c. Random Forest Regressor
Step 3. Classification
     3-a. Preparing Data
     3-b. One-Hot Encoding
     3-c. Logistic Regression
     3-d. KNN
     3-e. SVM
     3-f. GaussianNB
     3-g. Decision Tree
     3-h. Random Forest
     3-i. Perceptron
     3-j. Stochastic Gradient Descent (SGD)
     3-k. Ridge Regression
Step 4. Conclusion
```
---
**[10. Breast Cancer Prediction - 3 types(Basic, MinMaxScaled, StandardScaled) of comparison](https://github.com/sw-song/TIA/blob/main/10_Breast_Cancer_Wisconsin/Breast_Cancer_Prediction__with_3type_of_Data.ipynb)**
```
Step 1. Data Load & EDA & Preprocessing
Step 2. Visualization
     2-a. Correlation Heatmap - raw data
     2-b. Correlation Heatmap - MinMaxScaled data
     2-c. Correlation Heatmap - StandardScaled data
Step 3. Modeling & Prediction
     3-a. Logistic Regression - raw data
     3-b. SGDClassifier       - raw data
     3-c. Logistic Regression - MinMaxScaled data
     3-d. SGDClassifier       - MinMaxScaled data
     3-e. Logistic Regression - StandardScaled data
     3-f. SGDClassifier       - StandardScaled data
Step 4. Conclusion
```
 
**[10+. Breast Cancer Prediction - Clone Project(Feature Selection and Data Visualization)](https://github.com/sw-song/TIA/blob/main/10_Breast_Cancer_Wisconsin/Clone_Feature_Selection_and_Data_Visualization.ipynb)**
```
Step 1. Data Analysis
Step 2. Data Visualization
     2-a. violinplot
     2-b. boxplot
     2-c. jointplot
     2-d. pairgrid
     2-e. swarmplot
     2-f. heatmap
Step 3. Feature Selection and Random Forest Classification
     3-a. Feature selection with correlation and random forest classification
     3-b. Univariate feature selection and random forest classification
     3-c. Recursive feature elimination (RFE) with random forest
     3-d. Recursive feature elimination with cross validation (RFECV) and random forest classification
     3-e. Tree based feature selection and random forest classification
Step 4. Feature Extraction
Conclusion
```
---
**[11-(1). Simple NN Basic Model with Fasion MNIST](https://github.com/sw-song/TIA/blob/main/11_Fashion_mnist_classification/fasion_mnist_basic.ipynb)**
```
Step 0. Library Import
Step 1. Dataset Load and EDA
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate
```

**[11-(2). Fashion MNIST Classification and Visualization](https://github.com/sw-song/TIA/blob/main/11_Fashion_mnist_classification/fasion_mnist.ipynb)**
```
Step 1. Library Import & Load Dataset
     1-a. Library
     1-b. Datasets
     1-c. Shape of Data
     1-d. Show Image
Step 2. Data Preprocessing
     2-a. class name (y)
     2-b. Normalization (X)
     2-c. Visualization (X)
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Training
Step 6. Model Evaluation
Step 7. Prediction
     7-a. using predict method
     7-b. predict y
     7-c. visualization - Predict Class
     7-d. visualization - Predict target image
```
---
**[12. Simple NN Basic Model with iris dataset](https://github.com/sw-song/TIA/blob/main/12_iris_classification/iris_basic.ipynb)**
```
Step 0. Library Import
Step 1. Dataset Load
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate
```
---
**[13. Simple CNN Model with RPS dataset - val_loss : 0.0819](https://github.com/sw-song/TIA/blob/main/13_RPS_Image_Classification/RPS_basic_cnn.ipynb)**
```
Step 0. Library Import
Step 1. Dataset Load
Step 2. Data Generator
Step 3. Modeling
Step 4. Model Compile
Step 5. Save Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Reload Model
```
---
**[14-(1). Simple CNN Model with 'Horses or Humans' dataset - val_loss : 0.0181](https://github.com/sw-song/TIA/blob/main/14_Horses_or_Humans/horses_or_humans_classification.ipynb)**
> (High Accuracy, Incorrect assignment of test data)
```
Step 0. Library Import
Step 1. Dataset Load
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Svae
Step 8. Reload Model
```
**[14-(2). Simple CNN Model(&Sigmoid) with 'Horses or Humans' dataset - val_loss : 0.7197](https://github.com/sw-song/TIA/blob/main/14_Horses_or_Humans/horses_or_humans_classification_sigmoid.ipynb)**
```
Step 0. Library Import
Step 1. Dataset Load
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Svae
Step 8. Reload Model
```
**[14-(3). Simple CNN Model(&Sigmoid) with 'Horses or Humans' dataset (+callbacks, learning rate scheduler) - val_loss : 0.6627](https://github.com/sw-song/TIA/blob/main/14_Horses_or_Humans/horses_or_humans_classification_callbacks.ipynb)**
```
Step 0. Library Import
Step 1. Dataset Load
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Svae
Step 8. Reload Model
```
---
**[15-(1). Simple CNN Model with 'Cats vs Dogs' dataset - val_loss : 0.3119](https://github.com/sw-song/TIA/blob/main/15_Cats_vs_Dogs/cnn_3119/cats_vs_dogs_classification.ipynb)**
```
Step 0. Library Import
Step 1. Dataset Load
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Svae
Step 8. Reload Model
```
**[15-(2). VGG16 Transfer CNN Model with 'Cats vs Dogs' dataset - val_loss : 0.1579](https://github.com/sw-song/TIA/blob/main/15_Cats_vs_Dogs/vgg16_1579/cats_vs_dogs_classification_with_vgg16.ipynb)**
```
Step 0. Library Import
Step 1. Load Dataset
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Model Reload
```
---
**[16. Simple NLP Model with 'sarcasm' dataset - val_loss : 0.3687](https://github.com/sw-song/TIA/blob/main/16_sarcasm/sarcasm.ipynb)**
```
Step 0. Library Import
Step 1. Load Dataset
Step 2. Data Preprocessing
     2-a. Train/Test split
     2-b. Tokenizer
     2-c. Pad Sequences
     2-d. label type : list -> numpy array
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Reload Model
```
**[16+. Sarcasm in News Headlines Classification - Clone Project(Sarcasm Detection : A Guide for ML and DL approach)](https://github.com/sw-song/TIA/blob/main/16_sarcasm/Clone_sarcasm.ipynb)**
```
Step 1. Loading and Viewing the Sample Dataset
Step 2. ML Approach
Step 3. DL Approach

```
---
**[17. Time Series Forcasting Model based on LSTM with 'sunspots' dataset - val_mae : 13.90](https://github.com/sw-song/TIA/blob/main/17_sunspots/timeseries_sunspots.ipynb)**
```
Step 0. Library Import
Step 1. Load Dataset
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Model Reload
```

**[17+. Time Series Forcasting Model based on LSTM with 'sunspots' dataset - Clone Project(Time Series - TensorFlow RNN-LSTM Introduction)](https://github.com/sw-song/TIA/blob/main/17_sunspots/Clone_timeseries_sunspots.ipynb)**
```
Step 0. Library Import
Step 1. Load Dataset
Step 2. Data Preprocessing
Step 3. Modeling
Step 4. Model Compile
Step 5. Callbacks
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Model Reload
```
---
**[18-(1). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | Step-by-Step Tutorial From EDA To Preprocessing for Image Detection](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/step-by-step-tutorial-from-eda-to-preprocessing.ipynb)**
```
Step 1. Import Libraries
Step 2. Load Data
Step 3. Read DCM File
     3-a. explore path with python code
     3-b. make image extractor(function)
Step 4. Show Sample Image
     4-a. explore image data with python code
     4-b. check position to draw box
Step 5. Show Multiple Images
Step 6. Feature Engineering
     6-a. count opacity
     6-b. simplify 'id'
     6-c. rename colume 'id' to 'StudyInstanceUID for merge on 'StudyInstanceUID'
     6-d. check the relation between 'OpacityCount' and other columes in train_study
     6-e. visualize the relation between 'OpacityCount' and other columes in train_study
     6-f. check duplicate values(One row and Two Appearances)
```  

**[18-(2). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM Step by Step Image Detection for Beginners](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-step-by-step-image-detection-for-beginners.ipynb)**
```
Step 1. Import Libraries
Step 2. Load Data
Step 3. Read DCM File
     3-a. explore path with python code
     3-b. make image extractor(function)
Step 4. Show Sample Image
     4-a. explore image data with python code
     4-b. check position to draw box
Step 5. Show Multiple Images
Step 6. Feature Engineering I
     6-a. count opacity
     6-b. simplify 'id'
     6-c. rename colume 'id' to 'StudyInstanceUID for merge on 'StudyInstanceUID'
     6-d. check the relation between 'OpacityCount' and other columes in train_study
     6-e. visualize the relation between 'OpacityCount' and other columes in train_study
     6-f. check duplicate values(One row and Two Appearances)
Step 7. Feature Engineering II
     7-a. explore data analysis
     7-b. check duplicates in dataset
     7-c. modify some of the code in function that extract image(.dcm)
Step 8. Visualize X-ray with bbox
     8-a. negative for pneumonia
     8-b. typical appearance
     8-c. indeterminate appearance
     8-d. atypical Appearance
Step 9. Featrue Engineering III
     9 .. ing
```  

**[18-(3). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM-COVID-19 Detection - 10 Step Tutorial](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-10-step-tutorial.ipynb)**
```
Step 1. Import Libraries
Step 2. Load Data
Step 3. Read DCM File
     3-a. explore path with python code
     3-b. make image extractor(function)
Step 4. Show Sample Image
     4-a. explore image data with python code
     4-b. check position to draw box
Step 5. Show Multiple Images
Step 6. Feature Engineering I
     6-a. count opacity
     6-b. simplify 'id'
     6-c. rename colume 'id' to 'StudyInstanceUID for merge on 'StudyInstanceUID'
     6-d. check the relation between 'OpacityCount' and other columes in train_study
     6-e. visualize the relation between 'OpacityCount' and other columes in train_study
     6-f. check duplicate values(One row and Two Appearances)
Step 7. Feature Engineering II
     7-a. explore data analysis
     7-b. check duplicates in dataset
     7-c. modify some of the code in function that extract image(.dcm)
Step 8. Visualize X-ray with bbox
     8-a. negative for pneumonia
     8-b. typical appearance
     8-c. indeterminate appearance
     8-d. atypical Appearance
Step 9. Featrue Engineering III
     9-a. anomaly detection
     9-b. show outliers in `Typical Appearance`
     9-c. show outliers in `Intermiate Appearance`
     9-d. show outliers in `Atypical Appearance`
Step 10. Image Data Preprocessing
```  

**[18-(4). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM: COVID-19 Detection 🔱 10+Step Tutorial (1)](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-10-step-tutorial-1.ipynb)**
```
Step 1. Import Libraries
Step 2. Load Data
Step 3. Read DCM File
     3-a. explore path with python code
     3-b. make image extractor(function)
Step 4. Show Sample Image
     4-a. explore image data with python code
     4-b. check position to draw box
Step 5. Show Multiple Images
Step 6. Feature Engineering I
     6-a. count opacity
     6-b. simplify 'id'
     6-c. rename colume 'id' to 'StudyInstanceUID for merge on 'StudyInstanceUID'
     6-d. check the relation between 'OpacityCount' and other columes in train_study
     6-e. visualize the relation between 'OpacityCount' and other columes in train_study
     6-f. check duplicate values(One row and Two Appearances)
Step 7. Feature Engineering II
     7-a. explore data analysis
     7-b. check duplicates in dataset
     7-c. modify some of the code in function that extract image(.dcm)
Step 8. Visualize X-ray with bbox
     8-a. negative for pneumonia
     8-b. typical appearance
     8-c. indeterminate appearance
     8-d. atypical Appearance
Step 9. Featrue Engineering III
     9-a. anomaly detection
     9-b. show outliers in `Typical Appearance`
     9-c. show outliers in `Intermiate Appearance`
     9-d. show outliers in `Atypical Appearance`
Step 10. Image Data Preprocessing
     10-a. add image path to a separate column
     10-b. Resize the image (uniform to 150x150) and Scale each pixel values (uniform range 1~255)
     10-c. Calculate the resize ratio(x, y) and Apply the same to the bounding box
```  

**[18-(5). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM: COVID-19 Detection 🔱 10+Step Tutorial (2)](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-10-step-tutorial-2.ipynb)**
```
Step 1. Load Data and Trim for use
     1-a. load train-dataframe
     1-b. load meta-dataframe
     1-c. load image data array
     1-d. calculate image resize ratio information
Step 2. Image Pre-Classification with Data generator
     2-a. classify image id by opacity types
     2-b. sort image files into each type's folder
     2-c. data generation, split train/valid set
Step 3. Modeling - Multiclass classifier
     3-a. import libraries
     3-b. basic modeling with keras api
     3-c. model compile
     3-d. save model checkpoint
     3-e. model fit
     3-f. model evaluate & save
     3-g. reload model & model summary
```

**[18-(6). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM: COVID-19 Detection 🔱 10+Step Tutorial (2)](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-10-step-tutorial-2-2.ipynb)**
```
Step 1. Load Data and Trim for use
     1-a. load train-dataframe
     1-b. load meta-dataframe
     1-c. load image data array
     1-d. calculate image resize ratio information
Step 2. Image Pre-Classification with Data generator
     2-a. classify image id by opacity types
     2-b. sort image files into each type's folder
     2-c. data generation, split train/valid set
Step 3. Modeling I - Basic Multiclass classifier
     3-a. import libraries
     3-b. basic modeling with keras api
     3-c. model compile
     3-d. save model checkpoint
     3-e. model fit
     3-f. model evaluate & save
     3-g. reload model & model summary
Step 4. Modeling II - Multiclass classifier using EfficientNet(Transfer Learning)
     4-a. Load the EfficientNet and try it out
     4-b.  Improving performance with an appropriate form
```


**[18-(7). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | Tutorial : Multi-Output Regression](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/multi_output_regression_tutorial.ipynb)**
```
Step 1. Get the dataset
Step 2. Get the model
Step 3. Evaluate a model using repeated k-fold cross-validation
Step 4. Load dataset
Step 5. Evaluate model
Step 6. Practical Application
```

**[18-(8). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM: COVID-19 Detection 🔱 Mini Part - Preprocess](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-mini-part-preprocess.ipynb)**
```
Step 1. Import Dataset
Step 2. Test Sample data(1 row) before make the preprocessing function
     2-a. The image with the most opacity detected is taken as a sample
     2-b. visualize resized image without boxes
     2-c. extract position information
     2-d. Extract all box's information for sample image.
     2-e. Extract corrected positions that resizing ratio is calculated
     2-f. visualize resized image with boxes
Step 3. Build Function for reuse
     3-a. Test the functions that go into the function
     3-b. Build Function and Create New DataFrame with loop
     3-c. concat dataframe and save
```

**[18-(9). Archive For Kaggle Competition | SIIM-FISABIO-RSNA COVID-19 Detection | SIIM: COVID-19 Detection 🔱 MultiOutput Regression](https://github.com/sw-song/TIA/blob/main/18_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-multioutput-regression.ipynb)**
```
Step 1. Load Train Data Table
     1-a. extract data with only one opacity
     1-b. extract image paths
Step 2. Load Image Dataset
     2-a. Data Preprocessing
Step 3. Modeling
     3-a. Train-valid split
     3-b. Modeling
     3-c. Training
     3-d. Evaluation
 ```

---
 **[19+. Conditional GAN Basic with PyTorch - Clone Project(Conditional Generative Adversarial Network)](https://github.com/sw-song/TIA/blob/main/19_Conditional_GAN_Basic/clone-conditional-generative-adversarial-network.ipynb)**
```
Step 1. Load Data
     1-a. read csv
     1-b. x & y split
     1-c. data preprocessing - x
     1-d. data preprocessing - y 
     1-e. show sample image
Step 2. Modeling
     2-a. generator network
     2-b. discriminator network
     3-c. instantiate the networks
     3-d. moving the networks to the gpu
     3-e. create the loss function and optimizers
     3-f. creating network optimizing functions 
Step 3. Model Training
```

**[19-(1). Generate Fashion images with Conditional GAN ..ing](https://github.com/sw-song/TIA/blob/main/19_Conditional_GAN_Basic/generate-fashion-images-with-conditional-gan.ipynb)**
```
Step 1. Import Libraries and Load Dataset
     1-a. basic way to load dataset
     1-b. more efficient way to load dataset(with transform) + batch
Step 2. Define Discriminator and Generator
     2-a. discriminator
     2-b. generator
Step 3. Define Loss Function and Optimizing Function
     3-a. loss function
     3-b. optimizing function
Step 4. Define Training Functions
     4-a. training gerenator (get 1 loss and 1 gradient descent)
     4-b. training discriminator (get 1 loss and 1 gradient descent)
Step 5. Train Model
```

**[19-(2). Generate Fashion images with Conditional GAN - final](https://github.com/sw-song/TIA/blob/main/19_Conditional_GAN_Basic/generate-fashion-images-with-conditional-gan-final.ipynb)**
```
Step 1. Import Libraries and Load Dataset
     1-a. basic way to load dataset
     1-b. more efficient way to load dataset(with transform) + batch
Step 2. Define Discriminator and Generator
     2-a. discriminator
     2-b. generator
Step 3. Define Loss Function and Optimizing Function
     3-a. loss function
     3-b. optimizing function
Step 4. Define Training Functions
     4-a. training gerenator (get 1 loss and 1 gradient descent)
     4-b. training discriminator (get 1 loss and 1 gradient descent)
Step 5. Train Model
Step 6. Test Model
```
---
**[20+. Animal Face Classification with PyTorch - Clone Project(Pytorch Animal Face Classification - CNN)](https://github.com/sw-song/TIA/blob/main/20_PyTorch_Classification_Basic/clone-pytorch-animal-face-classification.ipynb)**
```
Step 1. Preparing Dataset
     1-a. Preparing Dataset Class
     1-b. Preparing Sampler Objects
     1-c. Preparing Data Loader Objects
Step 2. Neural Network Modeling
Step 3. Training Model
Step 4. Final Test
Step 5. Save a PyTorch Model
```

---
**[21. PyTorch Basic to CNN - Clone Project(Pytorch Tutorial for Deep Learning Lovers)](https://github.com/sw-song/TIA/blob/main/21_Pytorch_Neural_Net/clone-pytorch-tutorial-for-deep-learning-lovers.ipynb)**
```
Step 1. Basics of pytorch
Step 2. Linear regression with pytorch
Step 3. Logistic regression with pytorch
Step 4. Artificial neural network with pytorch
Step 5. Convolutional neural network with pytorch
```

---
**[22. GAN Basic Tutorial : Generate MNIST](https://github.com/sw-song/TIA/blob/main/22_PyTorch_GAN_MNIST/overview-of-basic-gan-architecture.ipynb)**
```
Step 1. Import Libraries
Step 2. Initial Setting
Step 3. Define Generator
Step 4. Define Discriminator
Step 5. Define Loss Function
Step 6. Initialize Generator and Discriminator
Step 7. GPU Setting
Step 8. Configure Data Loader
Step 9. Define Optimizers
Step 10. Training
```
---
**[23-(1). (blueprint)CycleGAN Tutorial : Monet to Photo](https://github.com/sw-song/TIA/blob/main/23_PyTorch_CycleGAN_Monet_to_Photo/cyclegan_tutorial_monet_to_photo.ipynb)**
```
Step 1. Import Libraries
Step 2. Initial Setting
Step 3. Define Generator
Step 4. Define Discriminator
Step 5. Define Loss Function
Step 6. Initialize Generator and Discriminator
Step 7. GPU Setting
Step 8. Weight Setting
Step 9. Configure Optimizer
Step 10. Learning Rate Scheduler Setting
Step 11. Image Transformation Setting
Step 12. DataLoader Setting
Step 13. Define function to get sample images
Step 14. Training
```

**[23-(2). (final)CycleGAN Tutorial : Monet to Photo](https://github.com/sw-song/TIA/blob/main/23_PyTorch_CycleGAN_Monet_to_Photo/final_cyclegan-tutorial-monet-to-photo.ipynb)**
```
Step 1. Import Libraries
Step 2. Initial Setting
Step 3. Define Generator
Step 4. Define Discriminator
Step 5. Define Loss Function
Step 6. Initialize Generator and Discriminator
Step 7. GPU Setting
Step 8. Weight Setting
Step 9. Configure Optimizer
Step 10. Learning Rate Scheduler Setting
Step 11. Image Transformation Setting
Step 12. DataLoader Setting
Step 13. Define function to get sample images
Step 14. Training
```
---

**[24-(1). (blueprint)StarGAN Tutorial : Generate Celeb Images](https://github.com/sw-song/TIA/blob/main/24_PyTorch_StarGAN_CelebA/stargan-tutorial-generate-celeb-images.ipynb)**
```
Step 1. Import Libraries
Step 2. Initial Setting
Step 3. Define Generator
Step 4. Define Discriminator
Step 5. Define Loss function and Initialize Loss weights
Step 6. Initialize Generator and Discriminator
Step 7. GPU Setting
Step 8. Weight Setting
Step 9. Configure Optimizers
Step 10. Set transforms and Configure DataLoaders
Step 11. Define Gradient Penalty Function
Step 12. Define function to get sample images with input label list
Step 13. Training
```

**[24-(2). (final)StarGAN Tutorial : Generate Celeb Images](https://github.com/sw-song/TIA/blob/main/24_PyTorch_StarGAN_CelebA/final_stargan-tutorial-generate-celeb-images.ipynb)**
```
Step 1. Import Libraries
Step 2. Initial Setting
Step 3. Define Generator
Step 4. Define Discriminator
Step 5. Define Loss function and Initialize Loss weights
Step 6. Initialize Generator and Discriminator
Step 7. GPU Setting
Step 8. Weight Setting
Step 9. Configure Optimizers
Step 10. Define CelebADataset Class for handling labeled dataset
Step 11. Set transforms and Configure Dataloader for training
Step 12. Set transforms and Configure Dataloader for testing
Step 13. Define Gradient Penalty Function
Step 14. Define function to get sample images with input label list
Step 15. Training
```
---

**[25. Image Generation using Stylegan pre-trained model](https://github.com/sw-song/TIA/blob/main/25_PyTorch_Stylegan_Using_Pre-trained-model/image-generation-using-stylegan-pre-trained-model.ipynb)**
```
Step 1. Import Libraries
Step 2. Design Layers
     2-a. linear layer
     2-b. convolution layer
     2-c. noise layer
     2-d. style modification layer
     2-e. pixel normalization layer
     2-f. blur layer
     2-g. upscaling layer
Step 3. Design Networks
     3-a. generator mapping network
     3-b. generator synthesis blocks
     3-c. generator synthesis network
Step 4. Define the Model (Image Generator)
     4-a. data flow : z to image
     4-b. load pre-trained weight
Step 5. Test the Model
     5-a. gpu setting
     5-b. input setting - grid
     5-c. input setting - latent z
     5-d. show samples
Step 6. Control Latent Vector
     6-a. first random latent vector + generate first image
     6-b. second random latent vector + generate second image
     6-c. half `z` + half `z`
     6-d. half `w` + half `w`
     6-e. Image Interpolation Comparison
```
---

**[26-(1). (Step ~2)Image Generation using Stylegan pre-trained model](https://github.com/sw-song/TIA/blob/main/26_Generate_Dog_with_StyleGAN2-ada/step1~2_stylegan2-ada.ipynb)**
```
Step 1. Initial Setting and load pre-trained model
     1-a. import libraries
     1-b. clone the stylegan2-ada's git repository
     1-c. load pre-trained model that trained on afhqdog dataset
Step 2. generate sample fake-dog images
     2-a. a quick look at the model
     2-b. try submodels : g_mapping, g_synthesis
```


**[26-(2). (Step ~3)Image Generation using Stylegan pre-trained model](https://github.com/sw-song/TIA/blob/main/26_Generate_Dog_with_StyleGAN2-ada/step+3_stylegan2-ada.ipynb)**
```
Step 1. Initial Setting and load pre-trained model
     1-a. import libraries
     1-b. clone the stylegan2-ada's git repository
     1-c. load pre-trained model that trained on afhqdog dataset
Step 2. generate sample fake-dog images
     2-a. a quick look at the model
     2-b. try submodels : g_mapping, g_synthesis
Step 3. image morphing
     3-a. create 2 random vector z and 2 intermediate latent space w
     3-b. generate 2 target fake-dog images
     3-c. control `z` and try image interpolation
```

**[26-(3). (Step ~4)Image Generation using Stylegan pre-trained model](https://github.com/sw-song/TIA/blob/main/26_Generate_Dog_with_StyleGAN2-ada/step+4_stylegan2-ada.ipynb)**
```
Step 1. Initial Setting and load pre-trained model
     1-a. import libraries
     1-b. clone the stylegan2-ada's git repository
     1-c. load pre-trained model that trained on afhqdog dataset
Step 2. generate sample fake-dog images
     2-a. a quick look at the model
     2-b. try submodels : g_mapping, g_synthesis
Step 3. image morphing
     3-a. create 2 random vector z and 2 intermediate latent space w
     3-b. generate 2 target fake-dog images
     3-c. control `z` and try image interpolation
Step 4. Project sample image to the latent space of pretrained network
     4-a. load a target image
     4-b. transform image file to numpy array
     4-c. load the pre-trained Generator
     4-d. Compute w stats
     4-e. Setup noise inputs
     4-f. Load VGG16 feature detector
     4-g. Extract features for target image
     4-h. Set optimizer and Initiate noise
     4-i. projection(training)
     4-j. Compare the target image with the generated image
Step 5. Change the characteristics of a new image
```

**[26-(4). StyleGAN2-ADA : Style Conversion - Changing A Dog's Facial Expression (master version of Image Generation using Stylegan pre-trained model)](https://github.com/sw-song/TIA/blob/main/26_Generate_Dog_with_StyleGAN2-ada/stylegan2-ada-change-a-dog-s-facial-expression.ipynb)**
```
Step 1. Initial Setting and load pre-trained model
     1-a. import libraries
     1-b. clone the stylegan2-ada's git repository
     1-c. load pre-trained model that trained on afhqdog dataset
Step 2. generate sample fake-dog images
     2-a. a quick look at the model
     2-b. try submodels : g_mapping, g_synthesis
Step 3. image morphing
     3-a. create 2 random vector z and 2 intermediate latent space w
     3-b. generate 2 target fake-dog images
     3-c. control `z` and try image interpolation
Step 4. Project sample image to the latent space of pretrained network
     4-a. load a target image
     4-b. transform image file to numpy array
     4-c. load the pre-trained Generator
     4-d. Compute w stats
     4-e. Setup noise inputs
     4-f. Load VGG16 feature detector
     4-g. Extract features for target image
     4-h. Set optimizer and Initiate noise
     4-i. projection(training)
     4-j. Compare the target image with the generated image
Step 5. Style Conversion
     5-a. Extract information about smiling expressions
     5-b. Import w to insert facial expressions
```

**[27+. Clone Project(bitcoin eda and forecasting using pycaret)](https://github.com/sw-song/TIA/blob/main/27_Crypto_Forecasting/clone-bitcoin-eda-and-forecasting-using-pycaret.ipynb)**
```
1. Importing dataset
2. Filtering bitcoin from dataset
   2-1. checking for null values
   2-2. dropping null values
   2-3. changing unix timestamp into date and time
3. Explanatory data analysis
   3-1. statistics of bitcoin
   3-2. some insights about bitcoin
   3-3. vwap as per time
   3-4. trading volume as per time
   3-5. the number of trades that took place as per time
   3-6. correlation
4. Using pycaret for forcasting close price of bitcoin
   4-1. installing pycaret
   4-2. setting up the model and comparing between different models
   4-3. plotting the best model
```

**[27+. Clone Project(Crypto Forecasting Tutorial) + translate](https://github.com/sw-song/TIA/blob/main/27_Crypto_Forecasting/crypto-forecasting-tutorial.ipynb)**
```
1. G-Research Crypto forecasting competition
   1-1. The Cryptocurrency Market(암호화폐 시장)
   1-2. Forecasting returns(수익 예측)
2. Dataset description(데이터셋 소개)
   2-1. Load the training set(학습 데이터 불러오기)
   2-2. Data features
   2-3. Candlestick charts(캔들 차트)
3. Preprocessing(전처리)
   3-1. Dealing with missing data(결측치 처리)
   3-2. Data visualization
   3-3. Log returns(로그 변환된 수익)
   3-4. Correlation between assets
4. Building your prediction model(예측 모델 구현)
   4-1. Prediction targets and evaluation
   4-2. Feature design
   4-3. Preparing the data for building predictive models
   4-4. Baseline model: Linear Regression(선형 회귀)
```
