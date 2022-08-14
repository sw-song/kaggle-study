
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

**[27+. Clone Project(Crypto Forecasting Tutorial) + translate](https://github.com/sw-song/TIA/blob/main/27_Crypto_Forecasting/crypto-forecasting-tutorial.ipynb)**
```
Step 1. G-Research Crypto forecasting competition
     1-1. The Cryptocurrency Market(암호화폐 시장)
     1-2. Forecasting returns(수익 예측)
Step 2. Dataset description(데이터셋 소개)
     2-1. Load the training set(학습 데이터 불러오기)
     2-2. Data features
     2-3. Candlestick charts(캔들 차트)
Step 3. Preprocessing(전처리)
     3-1. Dealing with missing data(결측치 처리)
     3-2. Data visualization
     3-3. Log returns(로그 변환된 수익)
     3-4. Correlation between assets
Step 4. Building your prediction model(예측 모델 구현)
     4-1. Prediction targets and evaluation
     4-2. Feature design
     4-3. Preparing the data for building predictive models
     4-4. Baseline model: Linear Regression(선형 회귀)
```

**[28. XGBoost Tutorial at AMEX Competition](https://github.com/sw-song/TIA/blob/main/28_XGBoost_AMEX/xgboost-tutorial.ipynb)**
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

**[29-(1). Let's Draw The Fracture More Clearly](https://github.com/sw-song/TIA/blob/main/29_Fracture_Detection/eda-let-s-draw-the-fracture-more-clearly.ipynb)**
```
Step 1. How to gather common ids and bounding-box infos?
Step 2. Draw some sample factures
Step 3. And.. Let's make Class
```

**[29-(2). Drawing 3D Cervical Spine](https://github.com/sw-song/TIA/blob/main/29_Fracture_Detection/break-time-just-enjoy-drawing-3d-cervical-spine.ipynb)**
```
Step 1. Load Libraries
Step 2. Set Data Path
Step 3. Get Path Of Nii Files
Step 4. Make The Class To Draw 3D Spines
```