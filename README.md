# Titanic-Survival-Prediction-using-Logistic-Regression

## Project Overview
This project involves a comprehensive analysis of the classic Titanic dataset. The primary goal is to perform Exploratory Data Analysis (EDA) to uncover factors that influenced passenger survival and then build a machine learning model to predict whether a passenger survived the disaster.

## Dataset
The project uses the Titanic dataset, which contains information about passengers such as their age, sex, passenger class, and whether they survived.

Part 1: Exploratory Data Analysis (EDA)
The initial analysis focused on cleaning the data, creating visualizations with matplotlib and seaborn, and deriving key insights.

## Key Findings from EDA:

**Gender**: Females had a significantly higher survival rate (74.2%) compared to males (18.9%), indicating the "women and children first" protocol was followed.

**Passenger Class (Pclass)**: Survival was strongly linked to class. First-class passengers had a ~63% survival rate, which dropped to ~47% for second-class and just ~24% for third-class passengers.

**Age**: Children had a notably higher survival rate than adults.

**Family Size**: Passengers traveling alone or in very large families had a lower chance of survival compared to those in small family groups of 2-4 members. This was determined by creating a Family_Size feature from the SibSp and Parch columns.

**Port of Embarkation**: Passengers from Cherbourg (C) had a higher survival rate, which was correlated with the higher average fare they paid, suggesting they were from a higher socioeconomic class.

## Part 2: Predictive Modeling
Based on the EDA, a predictive model was built to classify passenger survival.

**Modeling Steps:**

**Feature Engineering**: The Family_Size feature was created by combining the SibSp and Parch columns.

**Data Preprocessing:**

Unnecessary columns (Name, Ticket, Cabin) were dropped.

Categorical features (Sex, Embarked) were converted into numerical values.

Missing values in the Age and Embarked columns were filled using the median and mode, respectively.

**Model Training:**

The dataset was split into an 80% training set and a 20% testing set.

A Logistic Regression model was trained on the processed data. This algorithm is well-suited for binary classification tasks like this one.

## Results
The model's performance was evaluated on the unseen test data:

Accuracy: 80.4%

Confusion Matrix: The model correctly predicted the outcome for 144 out of 179 passengers in the test set.

True Positives (Survived): 54

True Negatives (Did not survive): 90

Classification Report: The model showed a good balance of precision (78%) and recall (73%) for predicting survivors.
