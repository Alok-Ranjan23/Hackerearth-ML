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



