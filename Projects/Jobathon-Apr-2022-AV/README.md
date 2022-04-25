# JOB-A-THON - April 2022 (Rank 25 on Private Board)
----------------------------------------------------------

## Demand Forecasting
-------------------------------------------
## Objective 
 - Can you forecast the demand of the car rentals on an hourly basis?
 ---------------------------------------------------------------------------
### Problem Statement
   ABC is a car rental company based out of Bangalore. It rents cars for both in and out stations at affordable prices. The users can rent different types of cars like Sedans, Hatchbacks, SUVs and MUVs, Minivans and so on.

  In recent times, the demand for cars is on the rise. As a result, the company would like to tackle the problem of supply and demand. The ultimate goal of the company is to strike the balance between the supply and demand inorder to meet the user expectations.

  The company has collected the details of each rental. Based on the past data, the company would like to forecast the demand of car rentals on an hourly basis. 
  
  #### Training Data
  -------------------------------------------
      August 2018 to February 2021.
      
  ### Approach
  ------------------------------------------------------------------
  
  #### Feature Extraction
  The data provides to us contain very less features.The features data contain basically Date , Demand and hour.
  So ,I am start the process with data extraction with help of panda date time features.I basically treat as regression problem.
  
  	date	hour	demand	year	month	day	weekday
  
  #### Exploratory Data Analysis
  
  ----------------------------------------------------------------------------
   ##### Distribution of Demand as per various Features   
  ![image](https://user-images.githubusercontent.com/95187592/165131962-de01b308-4e7c-4d40-85ab-f8144e5dd8bc.png)
  
  ![image](https://user-images.githubusercontent.com/95187592/165132046-dd86e402-0301-4ba6-89ec-298fd5bbfb8b.png)
  -------------------------------------------------------------
  
  ##### Outliers in DataSet
  ![image](https://user-images.githubusercontent.com/95187592/165132102-34f65e01-6bca-409f-a2de-b6db3ab2f84f.png)
  
  ##### Outliers in DataSet After treatment with z-score
  ![image](https://user-images.githubusercontent.com/95187592/165132141-970109ff-9745-4bfe-b654-e56914b31c24.png)
  ----------------------------------------------------------------
  ##### Distribution of Demand 
  ![image](https://user-images.githubusercontent.com/95187592/165132181-4697244b-dda6-4d5f-a0c7-a8f293f8e0c9.png)
  -------------------------------------------------------------------
  ##### Correlation Matrix
  
  ![image](https://user-images.githubusercontent.com/95187592/165132205-9356ddf3-65c7-4ab2-8609-eac00ee03a25.png)
  ---------------------------------------------------------------------------------
  
  ##### Trends in Demand with various time duration
  ![image](https://user-images.githubusercontent.com/95187592/165132228-4cdca03d-7320-4766-b828-c602cb8eee6f.png)
  ---------------------------------------------------------
  
  ![image](https://user-images.githubusercontent.com/95187592/165132254-e179667e-a1c3-40f4-98ef-5070ba81f1ba.png)
  ------------------------------------------------------------------------------------
  
  ![image](https://user-images.githubusercontent.com/95187592/165132281-abc1fc6c-1fe9-4627-9429-058ef2f8c545.png)
  --------------------------------------------------------------


### ML Approach
----------------------------------------
-----------------------------------------------

After doing feature extraction and enginering next step is machine learning.

- Cross Validation = Divided ny data into further train and test dataset.

-  Xgboost - does not perform well.
-  FbProphet -perform well as compare to XgBoost but poorer in compare to catboost.
-  CatBoostRegressor - Perform good intially , so For getting better result ,I decided to go for Hyperparameter Tunning with help of Grid Search Cv.The parameter finnaly used for Hyperparameter are following :
  - terations = 200 
  - l2_leaf_reg = 0.5
  - max_depth = 8
  - learning_rate = 0.1  
  - loss_function ='RMSE"
 - Model Score on validation Set - bestTest = 32.43745959
 - Public Score = 33.7218417593689	
 - Private Score = 33.58958531422
 
 ### Final Result
 ----------------------------------------
 Private Leaderboard - 25
 Public Leaderboard - 112
 


