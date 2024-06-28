## Project Name: *Credit Risk Analysis*

### Team Members: *Ramya Anand, Sunny, Jamil, Heidi Ye, Leslie wang*

The project of Team 1 is on 'Analysis of Credit Risk Data', the main intent of this project is to determine if the loan would be defaulted or not based on the loan parameters. There are totally 12 columns in the dataset, like loan_int_rate, loan_grade, person_credit_history, person_default history, loan_intent and so on. The loan_status is the column in the data set which is the dependent variable in determining if loan is defaulted or not. The factors are 'Y'/'N', 'Y' being loan gets defaulted and 'N' being not defaulted.

Below are the steps carried out in this project in order to successfully accomplish the above intent,

***Data Extraction***: The /data/raw folder holds the credit risk dataset fetched from Kaggle.com upon thorough analysis of data with good usability score like completeness of data, source credibility and data format compatibility. The dataset wasfrom licensed source with over 28000 records in csv file format with thorough column description and had an usability score of over 7 out of 10.

***Data PreProcess***: The raw data was cleaned up and pre processed before applying any analysis on the data. The ETL process has been carried out to extract the data from source, transform the data to clean null, Nan and duplicate values, rename columns to relevant names, change the data types and map data with relevant values in case of non numerical columns. The processed dataset is then saved into the /data/processed folder.

***Feature Analysis***: The data set has been applied with standard scaling technique to allocate equal weightage to every data column. The correlation between the columns has been verified to identify highly corelated columns and have them removed during the model analysis for correctly weighing the parameters. The data has been resampled using the bootstrapping technique to balance the data set. 
The main intent of the feature analysis was to understanding the loan features and the 'Loan Segmentation' on how loan_grade was classified and how is it different from the loan_status and the features that were contributing to decide the loan grade. The Kth nearest neighbour model was applied for fitting the data for this complex classification. This analysis helped in understanding the colinearity between some of the features which indirectly contributed to the loan default status determination and in selection of right set.

***Model Analysis***: Further to the feature analysis, which paved way for selection of appropriate features for the model analysis, the data set was fitted using various classification models to find out which model gave a good fit and best accuracy score. The experiments were as below,
  
  ***- Logical Regression model:***

  ***- Kth Nearest Neighbour:***
We trained the model using a train-test split approach, dividing the data into 80% for training and 20% for testing. This method is essential for accurately assessing the model's performance. The training set enables the model to learn patterns and relationships within the data, while the test set, unseen during training, is used to validate the model's ability to generalize and predict new data.

  ***- Random Forest model:***

***Model Validation***: The performance of a Random Forest model was evaluated using cross-validation with different numbers of folds to determine the optimal test condition. We first import necessary libraries and define a function, evaluate_model, which trains the Random Forest model and computes the accuracy using cross-validation. We explore a range of fold values from 5 to 25 and use K-Fold cross-validation with shuffling to ensure randomness. For each fold value, we calculate and print the mean accuracy along with the minimum and maximum accuracy observed across the folds. These values are recorded, and an error bar plot is generated to visualize the mean accuracies along with their respective error margins, indicating the stability and reliability of the model's performance across different cross-validation setups. 
