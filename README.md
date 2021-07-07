# Detect-fabrication-fault-in-Semiconductor-Wafers
Summary:
End to end ML project with Deployment. Data pipleline is created with data ingestion, data preprocessing, Model training and Model prediction

Problem Statement:
Based on mutiple sensor readings during a Semiconductor wafer manufacturing process, predict if a wafer can be calssified as good or bad

Solution(with approach):
1. New data is first validated againgst existing schema(regex pattern for name, number/name/datatype of column, null vlaues)
2. New data is inserted into the database. 
3. For Model training and predicition, dataset is read from database, followed by preprocessing(impute null values with KNN imputer, remove columns with constant values). 
Next, data is segmented into clusters with KMeans. 
4. For Model selection,  these clusters are then trained with Random Forest and XGBoost for each cluster. Highest AUC score metric used for best model. 
5. Model is deployed with RestAPI. 
