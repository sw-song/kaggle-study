## **Table of Contents**
```
Category 01. HR Analytics
Category 02. Marketing Analytics
Category 03. Climate & Environment Analytics
Category 04. Health & Medical Analytics
Category 05. Financial Analytics
Category 06. Learning Analytics
Category 07. Manufacture & Smart Factory
Category 08. Image Classification
Category 09. Sentiment Analysis
Category 10. Image Generation

```


---
## **Kernels**

### **Category 01. HR Analytics**

> **[1. HR Analytics: Job Change of Data Scientists](https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists)**


- **1-(1). Machine Learning for Beginner - HR Analytics | [Github](https://github.com/sw-song/TIA/blob/main/category_01_hr/01_HR_Analytics/HR_Analytics.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/machine-learning-for-beginner-hr-analytics/notebook)**
```
Step 1. Library Import
Step 2. Data Read
Step 3. EDA
Step 3-a. EDA - Visualization | Numerical Columns
Step 3-b. EDA - Visualization | Categorical Columns
Step 4. Split Train & Validation Set
Step 5. Train Model
Step 6. Evaluate Validation data Accuracy
```

- **1-(2). HR Analytics for begineer | [Github](https://github.com/sw-song/TIA/blob/main/category_01_hr/01_HR_Analytics/Clone__HR_Analytics_for_beginners.ipynb) | Kaggle(deleted)** *- by S P Rakshith*
```
Step 1. Importing the necessery libraries
Step 2. Importing the Data, head(), info()
Step 3. Checking the total number of Null Data - insa()
Step 4. Visualize the Categorical Data
Step 5. Modeling & Prediction
Step 6. Evaluation - Confusion Matrix
```

- **1-(3). Predict who will move to a new job | [Github](https://github.com/sw-song/TIA/blob/main/category_01_hr/01_HR_Analytics/Clone__Predict_who_will_move_to_a_new_job.ipynb) | [Kaggle](https://www.kaggle.com/code/khotijahs1/predict-who-will-move-to-a-new-job/notebook)** *- by Siti Khotijah*
```
Step 1. Import data
Step 2. Visualization
Step 3. Check missing Value and Replace Them with average of columns
Step 4. Type Tansfer - Categorical to Numerical
Step 5. Modeling & Prediction
Step 6. Evaluation - AUC
```

> **[2. Facebook Recruiting IV: Human or Robot?](https://www.kaggle.com/c/facebook-recruiting-iv-human-or-bot)**

- **2-(1). Anomaly Detection with XGB Classifier | [Github](https://github.com/sw-song/TIA/blob/main/category_01_hr/02_Classification_Human_or_Robot/Anomaly_Detection_with_XGBClassifier.ipynb)**
```
Step 1. Data load & EDA
Step 2. Preprocessing - replace all values with count number
Step 3. Preprocessing - Upsampling
Step 4. Train / Valid Set Split
Step 5. Modeling
Step 6. Prediction
```

---
### **Category 02. Marketing Analytics**
> **[1. Trending Youtube Video Statistics](https://www.kaggle.com/datasets/datasnaek/youtube-new?select=KRvideos.csv)**

- **1-(1). Youtube trend Analysis : Check Daily statistics for trending Youtube videos | [Github](https://github.com/sw-song/TIA/blob/main/category_02_marketing/01_Youtube_trend_Analysis/youtube_trend_analysis.ipynb)**
```
Step 1. Data Load & EDA
Step 2. Correlation Check - Heatmap
(+Time Series)
Step 3. Visualization - Numerical Columns
Step 4. Visualization - WordCloud
Step 5. Machine Learning Modeling(Keras)
```

> **2. Telecom Users Dataset Analysis(Deleted)**

- **2-(1). Logistic Regression - Step by Step | [Github](https://github.com/sw-song/TIA/blob/main/category_02_marketing/02_Telecom_users_analysis/quick-start-eda-to-machine-learning-logistic.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/logistic-regression-step-by-step)**
```
Step 1. Data Load & EDA
Step 2. Data Preprocessing
Step 3. Dataset Split(Train : Test = 0.8 : 0.2)
Step 4. Modeling : Logistic Regression
```

- **2-(2).EDA and Building models for predicting outflow | [Github](https://github.com/sw-song/TIA/blob/main/category_02_marketing/02_Telecom_users_analysis/Clone_EDA_and_Building_models_for_predicting_outflow.ipynb) | [Kaggle](https://www.kaggle.com/code/hijest/eda-and-building-models-for-predicting-outflow)** *- by radmirkaz*
```
Step 1. Data Description
Step 2. Dependency research and formulation of hypothesis
Step 3. Building models to predict outflow
```


---
### **Category 03. Climate & Environment Analytics**
> **[1. Natural Language Processing with Disaster Tweets](https://www.kaggle.com/c/nlp-getting-started/)**

- **1-(1). Quick Start NLP with Disaster Tweets | [Github](https://github.com/sw-song/TIA/blob/main/category_03_climate_environment/01_NLP_with_Disaster_Tweets/nlp_disaster_tweets.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/quick-start-nlp-with-disaster-tweets/notebook)**
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

- **1-(2). NLP Getting Started Tutorial | [Github](https://github.com/sw-song/TIA/blob/main/category_03_climate_environment/01_NLP_with_Disaster_Tweets/Clone_NLP_Getting_Started_Tutorial.ipynb) | [Kaggle](https://www.kaggle.com/code/philculliton/nlp-getting-started-tutorial)** *- by Phill Culliton*
```
Step 1. Data Load & EDA
Step 2. Text -> Vectorization(One Hot Encoding)
Step 3. Cross Validation Check
Step 4. Modeling
Step 5. Save / Submission(kaggle)
```

- **1-(3). Transfer Learning using TFHub | [Github](https://github.com/sw-song/TIA/blob/main/category_03_climate_environment/01_NLP_with_Disaster_Tweets/Clone_TL_using_TFHub.ipynb) | [Kaggle](https://www.kaggle.com/code/barun2104/transfer-learning-using-tfhub)** *- by Barun Kumar*

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

> **[2. Sunspots](https://www.kaggle.com/datasets/robervalt/sunspots)**

- **2-(1). Time Series Forcasting Model based on LSTM | [Github](https://github.com/sw-song/TIA/blob/main/category_03_climate_environment/02_sunspots/timeseries_sunspots.ipynb)**
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

- **2-(2)TensorFlow RNN-LSTM Introduction | [Github](https://github.com/sw-song/TIA/blob/main/category_03_climate_environment/02_sunspots/Clone_timeseries_sunspots.ipynb) | [Kaggle](https://www.kaggle.com/code/kutaykutlu/time-series-tensorflow-rnn-lstm-introduction)** *- by Kutay Kutlu*
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
### **Category 04. Health & Medical Analytics**
> **[1. Heart Attack Analysis & Prediction Dataset](https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset)**

- **1-(1). Binary Classification with Logistic Regression | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/05_Heart_Attack_Analysis_and_Prediction/quick-start-Binary_Classification_with_Logistic_Regression.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/binary-classification-with-logistic-regression/notebook)**
```
Step 1. Data Description
Step 2. EDA
Step 3. Correlation Check
Step 4. Test Data Split and Standard Scaling (Test size = 0.3)
Step 5. Modeling and Prediction
```

- **1-(2). Heart Attack Prediction | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/01_Heart_Attack_Analysis_and_Prediction/Clone_Heart_attack_prediction.ipynb) | [Kaggle](https://www.kaggle.com/code/avibagul80/heart-attack-prediction)** *-by Avinash Bagul*
```
Step 1. Data Description - missingno
Step 2. EDA - pandas_profiling
Step 3. Data preprocessing - remove Outlier, upsampling
Step 4. modeling / prediction / evaluation
Step 5. check feature importance
```

> **[2. Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)**

- **2-(1). Stroke Prediction with Easy Ensemble | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/02_Stroke_Prediction/stroke_prediction.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/stroke-prediction-with-easy-ensemble-acc-90)**
```
Step 1. Data Load & EDA
Step 2. Feature Engineering
     2-a. Binary Features
     2-b. Continuous Features
     2-c. Categorical Features
Step 3. Train / Test set Split & Upsampling
Step 4. Modeling & Prediction
```

- **2-(2). Stroke Prediction Beginner's Guide | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/02_Stroke_Prediction/Clone_stroke_prediction.ipynb) | [Kaggle](https://www.kaggle.com/code/sprakshith/stroke-prediction-beginner-s-guide)** *- by Rakshith S P*
```
Step 1. Importing the necessary libraries
Step 2. Importing the Data using Pandas read_csv(). And calling head() and info() on the DataFrame
Step 3. Preprocessing Data before Exploratory Data Analysis
Step 4. Exploratory Data Analysis on Stroke Prediction Data
Step 5. Preparing the Data for Prediction
Step 6. Creating a Model for Stroke Prediction
```

> **[3. Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)**

- **3-(1). Practice Preprocessing with Logistic, SGD Predict | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/03_Breast_Cancer_Wisconsin/Breast_Cancer_Prediction__with_3type_of_Data.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/practice-preprocessing-with-logistic-sgd-predict)**
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
 
- **3-(2). Feature Selection and Data Visualization | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/03_Breast_Cancer_Wisconsin/Clone_Feature_Selection_and_Data_Visualization.ipynb) | [Kaggle](https://www.kaggle.com/code/kanncaa1/feature-selection-and-data-visualization)** *- by DATAI*
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

> **[4. SIIM-FISABIO-RSNA COVID-19 Detection](https://www.kaggle.com/competitions/siim-covid19-detection/overview)**

- **4-(1). SIIM: COVID-19 Detection 🔱 10+Step Tutorial (1) | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/04_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-10-step-tutorial-1.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/siim-covid-19-detection-10-step-tutorial-1)**
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

- **4-(2). SIIM: COVID-19 Detection 🔱 10+Step Tutorial (2) | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/04_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-10-step-tutorial-2-2.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/siim-covid-19-detection-10-step-tutorial-2)**
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

- **4-(3). SIIM: COVID-19 Detection 🔱 Mini Part - Preprocess | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/04_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-mini-part-preprocess.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/siim-covid-19-detection-mini-part-preprocess)**
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

- **4-(4). SIIM: COVID-19 Detection 🔱 MultiOutput Regression | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/04_SIIM-FISABIO-RSNA_COVID-19_Detection/siim-covid-19-detection-multioutput-regression.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/siim-covid-19-detection-multioutput-regression)**
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

>**[5. RSNA 2022 Cervical Spine Fracture Detection](https://www.kaggle.com/competitions/rsna-2022-cervical-spine-fracture-detection)**

- **5-(1). Let's Draw The Fracture More Clearly | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/05_Fracture_Detection/eda-let-s-draw-the-fracture-more-clearly.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/eda-let-s-draw-the-fracture-more-clearly/data)**
```
Step 1. How to gather common ids and bounding-box infos?
Step 2. Draw some sample factures
Step 3. And.. Let's make Class
```

- **5-(2). Drawing 3D Cervical Spine | [Github](https://github.com/sw-song/TIA/blob/main/category_04_health_medical/05_Fracture_Detection/break-time-just-enjoy-drawing-3d-cervical-spine.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/break-time-just-enjoy-drawing-3d-cervical-spine)**
```
Step 1. Load Libraries
Step 2. Set Data Path
Step 3. Get Path Of Nii Files
Step 4. Make The Class To Draw 3D Spines
```

---
### **Category 05. Financial Analytics**

> **[1. Company Bankruptcy Prediction](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction)**

- **1-(1). Bankrupty Prediction for ML newbie | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/01_Company_Bankruptcy_Prediction/Bankruptcy_Prediction_with_KNN.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/for-ml-newbie-bankruptcy-prediction-accuracy-97)**
```
Step 1. Data Description
Step 2. Data Preprocessing - MinMaxScaling
Step 3. Machine Learning Modeling & Prediction
```

- **1-(2). Simple, yet, Powerful Bankrupt Prediction Model | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/01_Company_Bankruptcy_Prediction/Clone_Powerful_Bankrupt_Prediction.ipynb) | [Kaggle](https://www.kaggle.com/code/jaimebecerraguerrero/simple-yet-powerful-bankrupt-prediction-model)** *-by Jaime Becerra Guerrero*
```
Step 1. Data Loading and Data Cleaning
Step 2. Model Based Feature Selection
Step 3. Descriptive Analysis
Step 4. Data Analysis
Step 5. Predicting bankruptcy
Step 6. Conclusions
```

> **[2. G-Research Crypto Forecasting](https://www.kaggle.com/competitions/g-research-crypto-forecasting)**

- **2-(1). bitcoin eda and forecasting using pycaret | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/02_Crypto_Forecasting/clone-bitcoin-eda-and-forecasting-using-pycaret.ipynb) | 
[Kaggle](https://www.kaggle.com/code/pralabhpoudel/bitcoin-eda-and-forcasting-using-pycaret/notebook)** *- by Pralabh Poudel*
```
Step 1. Importing dataset
Step 2. Filtering bitcoin from dataset
     2-1. checking for null values
     2-2. dropping null values
     2-3. changing unix timestamp into date and time
Step 3. Explanatory data analysis
     3-1. statistics of bitcoin
     3-2. some insights about bitcoin
     3-3. vwap as per time
     3-4. trading volume as per time
     3-5. the number of trades that took place as per time
     3-6. correlation
Step 4. Using pycaret for forcasting close price of bitcoin
     4-1. installing pycaret
     4-2. setting up the model and comparing between different models
     4-3. plotting the best model
```

- **2-(2). Crypto Forecasting Tutorial | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/02_Crypto_Forecasting/crypto-forecasting-tutorial.ipynb) | [Kaggle(kr)](https://www.kaggle.com/code/songseungwon/crypto-forecasting-tutorial) | [Kaggle(en)](https://www.kaggle.com/code/cstein06/tutorial-to-the-g-research-crypto-competition/notebook)** *- by Carlos Stein N Brito*
```
Step 1. G-Research Crypto forecasting competition
     1-1. The Cryptocurrency Market
     1-2. Forecasting returns
Step 2. Dataset description
     2-1. Load the training set
     2-2. Data features
     2-3. Candlestick charts
Step 3. Preprocessing
     3-1. Dealing with missing data
     3-2. Data visualization
     3-3. Log returns
     3-4. Correlation between assets
Step 4. Building your prediction model
     4-1. Prediction targets and evaluation
     4-2. Feature design
     4-3. Preparing the data for building predictive models
     4-4. Baseline model: Linear Regression
```

>**[3. American Express - Default Prediction](https://www.kaggle.com/competitions/amex-default-prediction)**

- **3-(1). XGBoost Tutorial at AMEX Competition | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/03_XGBoost_AMEX/xgboost-tutorial.ipynb) | [Kaggle(kr)](https://www.kaggle.com/code/songseungwon/xgboost-tutorial) | [Kaggle(en)](https://www.kaggle.com/code/cdeotte/xgboost-starter-0-793)** *-by Chris Deotte*
```
Step 1. Load Libraries
Step 2. Load Dataset
Step 3. Feature Engineering
Step 4. Train XGB
Step 5. Save OOF Preds
Step 6. Feature Importances
Step 7. Process and Feature Engineer Test Data
Step 8. Infer Test
Step 9. Create Submission CSV
```

- **3-(2) De-Identified Data Analysis Tutorial | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/03_XGBoost_AMEX/de-identified-data-analysis-tutorial-ch-01.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/de-identified-data-analysis-tutorial-ch-01)**
```
Step 1. Load Samle Data
Step 2. Separate Data
Step 3. Check Outliers
Step 4. PCA (Focus on 'D' type)
```

- **3-(3) XGBoost Tutorial with Efficient Memory Management | [Github](https://github.com/sw-song/TIA/blob/main/category_05_finance/03_XGBoost_AMEX/xgboost-tutorial-with-efficient-memory-management.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/xgboost-tutorial-with-efficient-memory-management)**
```
1. Load Libraries
2. Load Dataset and Manage the GPU Memory
3. Feature Engineering
4. Train XGB
5. Save OOF Preds
6. Feature Importance
7. Data Processing and Feature Engineering for Test Data
8. Infer Test
9. Create Submission CSV
```


---
### **Category 06. Learning Analytics**
> **[1. Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)**


- **1-(1). MultiOutputRegression with Sparse X | [Github](https://github.com/sw-song/TIA/blob/main/category_06_learning/01_Students_Performance_in_Exams/_Students_Performance_in_Exams/Predict_Students_Performance.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/multioutputregression-with-sparse-x)**
```
Step 1. Data Load & EDA
Step 2. Visualization
     2-1. Each X's distribution
     2-2. Each y's distribution
     2-3. 'X & y's distribution
Step 3. Data Preprocessing
Step 4. Modeling & Prediction
```

- **1-(2). Data Science Notes 4: Machine Learning | [Github](https://github.com/sw-song/TIA/blob/main/category_06_learning/01_Students_Performance_in_Exams/Clone_Data_Science_Notes_4.ipynb) | [Kaggle](https://www.kaggle.com/code/mrhippo/data-science-notes-4-machine-learning-ml/notebook)** *- by Salih Albayrak*
```
Step 1. Imports and Datasets
Step 2. Regression
     2-1. Linear Regression 
     2-2. Decision Tree Regressor
     2-3. Random Forest Regressor
Step 3. Classification
     3-1. Preparing Data
     3-2. One-Hot Encoding
     3-3. Logistic Regression
     3-4. KNN
     3-5. SVM
     3-6. GaussianNB
     3-7. Decision Tree
     3-8. Random Forest
     3-9. Perceptron
     3-10. Stochastic Gradient Descent (SGD)
     3-11. Ridge Regression
Step 4. Conclusion
```

### **Category 07. Manufacture & Smart Factory**
> **[1. Fashion MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist)**

- **1-(1). Simple NN Basic Model with Fasion MNIST | [Github](https://github.com/sw-song/TIA/blob/main/category_07_manufacture/01_Fashion_mnist_classification/fasion_mnist_basic.ipynb)**
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

- **1-(2). Fashion MNIST Classification and Visualization | [Github](https://github.com/sw-song/TIA/blob/main/category_07_manufacture/01_Fashion_mnist_classification/fasion_mnist.ipynb)**
```
Step 1. Library Import & Load Dataset
     1-1. Library
     1-2. Datasets
     1-3. Shape of Data
     1-4. Show Image
Step 2. Data Preprocessing
     2-1. class name (y)
     2-2. Normalization (X)
     2-3. Visualization (X)
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Training
Step 6. Model Evaluation
Step 7. Prediction
     7-1. using predict method
     7-2. predict y
     7-3. visualization - Predict Class
     7-4. visualization - Predict target image
```

### **Category 08. Image Classification**
> **[1. Iris Species](https://www.kaggle.com/datasets/uciml/iris)**

- **1-(1). Simple NN Basic Model with iris dataset | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/01_iris_classification/iris_basic.ipynb)**
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

**[2. Rock-Paper-Scissors Images](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors?datasetId=107582&sortBy=voteCount)**

- **2-(1). Simple CNN Model with RPS dataset - val_loss : 0.0819 | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/02_RPS_Image_Classification/RPS_basic_cnn.ipynb)**
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

> **[3. Horses or Humans Dataset](https://www.kaggle.com/datasets/sanikamal/horses-or-humans-dataset)**

- **3-(1). Simple CNN Model | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/03_Horses_or_Humans/horses_or_humans_classification.ipynb)**
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
- **3-(2). Simple CNN Model + Sigmoid func | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/03_Horses_or_Humans/horses_or_humans_classification_sigmoid.ipynb)**
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
- **3-(3). Simple CNN Model + Sigmoid func +callbacks + learning rate scheduler | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/03_Horses_or_Humans/horses_or_humans_classification_callbacks.ipynb)**
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

> **[4. Cats vs Dogs](https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset)**

- **4-(1). Simple CNN Model | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/04_Cats_vs_Dogs/cnn_3119/cats_vs_dogs_classification.ipynb)**
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
- **4-(2). VGG16 Transfer CNN Model | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/04_Cats_vs_Dogs/vgg16_1579/cats_vs_dogs_classification_with_vgg16.ipynb)**
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

> **[5. Animal Faces](https://www.kaggle.com/datasets/andrewmvd/animal-faces)**

- **5-(1). Pytorch Animal Face Classification - CNNs | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/05_PyTorch_Classification_Basic/clone-pytorch-animal-face-classification.ipynb) | [Kaggle](https://www.kaggle.com/code/mehmetlaudatekman/pytorch-animal-face-classification-cnns/notebook)** *- by Mehmet Tekman*
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


> **[6. Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer)**

- **6-(1). Pytorch Tutorial for Deep Learning Lovers | [Github](https://github.com/sw-song/TIA/blob/main/category_08_image_classification/06_Pytorch_Neural_Net/clone-pytorch-tutorial-for-deep-learning-lovers.ipynb) | 
[Kaggle](https://www.kaggle.com/code/kanncaa1/pytorch-tutorial-for-deep-learning-lovers)** *- by DATAI*
``` 
Step 1. Basics of pytorch
Step 2. Linear regression with pytorch
Step 3. Logistic regression with pytorch
Step 4. Artificial neural network with pytorch
Step 5. Convolutional neural network with pytorch
```

---
### **Category 09. Sentiment Analysis**

> **[1. News Headlines Dataset For Sarcasm Detection](https://www.kaggle.com/datasets/rmisra/news-headlines-dataset-for-sarcasm-detection)**

- **1-(1). Simple NLP Model with 'sarcasm' dataset | [Github](https://github.com/sw-song/TIA/blob/main/category_09_sentiment_analysis/01_sarcasm/sarcasm.ipynb)**
```
Step 0. Library Import
Step 1. Load Dataset
Step 2. Data Preprocessing
     2-1. Train/Test split
     2-2. Tokenizer
     2-3. Pad Sequences
     2-4. label type : list -> numpy array
Step 3. Modeling
Step 4. Model Compile
Step 5. Model Checkpoint
Step 6. Model Fit
Step 7. Model Evaluate & Save
Step 8. Reload Model
```
- **1-(2). Sarcasm Detection : A Guide for ML and DL approach | [Github](https://github.com/sw-song/TIA/blob/main/category_09_sentiment_analysis/01_sarcasm/Clone_sarcasm.ipynb) | [Kaggle](https://www.kaggle.com/code/subbhashit/sarcasm-detection-a-guide-for-ml-and-dl-approach/notebook)** *- by Bunty*
```
Step 1. Loading and Viewing the Sample Dataset
Step 2. ML Approach
Step 3. DL Approach
```
---
### **Category 10. Image Generation**

> **[1. Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer)**

 - **1-(1). Conditional Generative Adversarial Network | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/01_mnist/clone-conditional-generative-adversarial-network.ipynb) | [Kaggle](https://www.kaggle.com/code/arpandhatt/conditional-generative-adversarial-network/notebook)** *- by Arpan Dhatt*
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


- **1-(2). PyTorch GAN Basic Tutorial for Beginner | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/01_mnist/overview-of-basic-gan-architecture.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/pytorch-gan-basic-tutorial-for-beginner)**
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

> **[2. Fashion MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist)**

- **2-(1). Generate Fashion images with Conditional GAN | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/02_fashion_mnist/generate-fashion-images-with-conditional-gan-final.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/generate-fashion-images-with-conditional-gan)** 
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

> **[3. I’m Something of a Painter Myself](https://www.kaggle.com/competitions/gan-getting-started)**


- **3-(1). CycleGAN Tutorial From Scratch: Monet-to-Photo | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/03_monet/final_cyclegan-tutorial-monet-to-photo.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/cyclegan-tutorial-from-scratch-monet-to-photo/data)**
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

> **[4. CelebFaces Attributes (CelebA) Dataset](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset)**

- **4-(1). StarGAN Tutorial with 15 Steps: Make Fake Images | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/04_celeb_a/final_stargan-tutorial-generate-celeb-images.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/stargan-tutorial-with-15-steps-make-fake-images)**
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

> **[5. FFHQ Face Data Set](https://www.kaggle.com/datasets/greatgamedota/ffhq-face-data-set)**

- **5-(1). Image Generation using Stylegan pre-trained model | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/05_ffhq/image-generation-using-stylegan-pre-trained-model.ipynb) | [Kaggle](https://www.kaggle.com/code/songseungwon/image-generation-using-stylegan-pre-trained-model)**
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

> [6. Animal Faces](https://www.kaggle.com/datasets/andrewmvd/animal-faces)

- **6-(1). [Stylegan2-ada]Change a dog's facial expression | [Github](https://github.com/sw-song/TIA/blob/main/category_10_image_generation/06_Generate_Dog_with_StyleGAN2-ada/stylegan2-ada-change-a-dog-s-facial-expression.ipynb)**
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
