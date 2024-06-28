## Project Name: *Credit Risk Analysis*

### Team Members: *Ramya Anand, Sunny Duggal, Jamil, Heidi Ye, Leslie wang*

The project of Team 1 is on 'Analysis of Credit Risk Data', the main intent of this project is to determine if the loan would be defaulted or not based on the loan parameters. There are totally 12 columns in the dataset, like loan_int_rate, loan_grade, person_credit_history, person_default history, loan_intent and so on. The loan_status is the column in the data set which is the dependent variable in determining if loan is defaulted or not. The factors are 'Y'/'N', 'Y' being loan gets defaulted and 'N' being not defaulted.

Below are the steps carried out in this project in order to successfully accomplish the above intent,

***Data Extraction***: The /data/raw folder holds the credit risk dataset fetched from Kaggle.com upon thorough analysis of data with good usability score like completeness of data, source credibility and data format compatibility. The dataset is a licensed source with over 28000 records in csv file format with thorough column description and had an usability score of over 7 out of 10.

***Data PreProcess***: The raw data has been cleaned up and pre processed before applying any analysis upon the data. Carried out the ETL process to extract the data from source, transform the data to clean null, Nan and duplicate values, rename columns to relevant names, change the data types and map data with relevant values in case of non numerical columns. The data has also been made free from any extreme outliers and saving it into the /data/processed folder.

***Feature Analysis***: The data set has been applied with standard scaling technique to allocate equal weightage to every data column. The correlation between the columns has been verified to identify highly corelated columns and have them removed during the model analysis for correctly weighing the parameters. The data has been resampled using the bootstrapping technique to balance the data set. 
The main intent of the feature analysis is to understand the loan features and the 'Loan Segmentation' on how loan_grade is classified and how is it different from the loan_status and the features that are contributing to decide the loan grade. The K-Nearest Neighbors model has been applied for this complex classification, which helped in understanding the collinearity between some of the features which indirectly contributed to the loan default status determination and in selection of the right feature set.

***Model Analysis***: Further to the feature analysis, which paved way for selection of appropriate features for the model analysis, the data set was fitted using various classification models to find out which model gave a good fit and best accuracy score. The experiments were as below,
  
  ***- Kth Nearest Neighbor:***
Starting with the KNN approach, we trained the model using a train-test split approach, dividing the data into 80% for training and 20% for testing. This method is essential for accurately assessing the model's performance. The training set enables the model to learn patterns and relationships within the data, while the test set, unseen during training, is used to validate the model's ability to generalize and predict new data. With an accuracy of about 84.26% for a best K value of 11, this model gave good results.

  ***- Logical Regression model:***
  Moving on to the Logistic regression, we tried different approaches, such as, using all the variables except loan status as the predictor variables, using only the statistically significant variables, using all except the loan interest because of its high correlation with the loan grade. We did this to identify the best model based on the accuracy number of the results. With all the different approaches having an accuracy of around 78%, Logistic regression shows the lowest performance, indicating it might not be the best fit for this dataset.

  ***- Random Forest model:***
  Finally, with an accuracy of around 93.2%, Random Forest Classifier stands out as one of the best. It also achieves perfect training accuracy indicating it generalizes well and handles overfitting better than the other two.

***Model Validation***: The performance of a Random Forest model was evaluated using cross-validation with different numbers of folds to determine the optimal test condition. We first import necessary libraries and define a function, evaluate_model, which trains the Random Forest model and computes the accuracy using cross-validation. We explore a range of fold values from 5 to 25 and use K-Fold cross-validation with shuffling to ensure randomness. For each fold value, we calculate and print the mean accuracy along with the minimum and maximum accuracy observed across the folds. These values are recorded, and an error bar plot is generated to visualize the mean accuracies along with their respective error margins, indicating the stability and reliability of the model's performance across different cross-validation setups. 

## Links to the video recordings

Heidi Ye: https://youtu.be/ug8WtpZy0y0
