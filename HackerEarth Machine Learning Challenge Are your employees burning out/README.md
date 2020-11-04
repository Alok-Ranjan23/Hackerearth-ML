# Predict the employee burn out rate

### Problem Statement
World Mental Health Day is celebrated on October 10 each year. The objective of this day is to raise an awareness about mental health issues around the world and mobilise
efforts in support of mental health. According to an anonymous survey, about 450 million people live with mental disorders that can be one of the primary causes of poor health
and disability worldwide.
You are a Machine Learning engineer in a company. You are given a task to understand and observe the mental health of all the employees in your company. Therefore, you are
required to predict the burn out rate of employees based on the provided features thus helping the company to take appropriate measures for their employees.

### Data
* train.csv (22750 x 9)
* test.csv (12250 x 8)
* sample_submission.csv (5 x 2)

### Variable Description
* Employee ID	-- Unique Id of the employee
* Date of Joining	-- Date on which the employee joined the company
* Gender	-- Gender of the employee
* Company Type	-- Type of company eg: Service based, product based etc.
* WFH -- Setup Available	Whether proper work from home setup is available or not 
* Designation	-- Seniority level of the employee in codes
* Resource Allocation -- Hours allocated per day
* Mental Fatigue Score	-- Stress rating provided by employees
* Burn Rate	-- Rate of saturation or burn out rate [Target]

### Submission format
Required to write your predictions in a .csv file that contain the following columns:
* Employee ID
* Burn Rate

### Evaluation criteria
The evaluation metric that is used for this problem is the r2_score. The formula is as follows:

 score=100*r2\_score(actual\_values, predicted\_values)
 
 ### Approach
 * Read the train and test dataset.
 #### Data Pre-processing
 * Check for the <b>NULL values.</b>
 * Romove rows where target is not present in train dataset.
 * Fill the Resource Allocation null value with median.
 * Train a linear regressor model to predict the null value for Metal Fatigue Score using Designation and Resource Allocation as features.
 * Handle the date of Joining : Get_Experience -- (today - Date of joining)
 * Handles Categorical Features : Gender, Company Type, WFH.
 * Drop Employee ID for train and test dataset. <b>But keep track for test Employee ID.</b>
 * Apply Min-max normalization for 'Experience, Designation, Resource Allocation, Mental Fatigue Score' in test as well as train dataset.
 #### Model Selection : Statistical model
 * Drop Target from train dataset.
 * Create a validation split from train and label with validation data having 20% of train dataset.
 * Create Baseline for following models and test them on validation split.
 * <b>Linear Regression</b>
 * <b>Support Vector Regression</b>
 * <b>Ridge Regression</b>
 * <b>Lasso Regression</b>
 * Selected baseline models are <b>Linear Regression</b> and <b>Ridge Reression</b>.
 * <b>GridSearchCV with k-fold cross validation(k=5)</b> of sklearn is used for an exhaustive serach of hyperparameter in case of Linear Regression model and Ridge Regression model.
 * Ridge Regression model is selected with its optimal hyper-parameter settings.
 * The whole train dataset and labels are used to train the <Ridge Regression model> with its optimal hyper-parameter settings.
 * The prediction is created for test dataset and written in submission.csv using the <b>trained Ridge Regression Model.</b>
 * The preformance criterion is r2-score here.
 * The achieved score is <b>92.23439</b>(i.e. 100*r2-score(y_actual,y_prediction))



