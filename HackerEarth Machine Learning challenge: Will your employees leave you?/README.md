### Problem Statement: -
Employees are the most important part of an organization. Successful employees meet deadlines, make sales, and build the brand through 
positive customer interactions.

Employee attrition is a major cost to an organization and predicting such attritions is the most important requirement of the Human 
Resources department in many organizations. In this problem, your task is to predict the attrition rate of employees of an organization.

### Data Description: -

 * Employee_ID	- Unique ID of each employee
 * Age -	Age of each employee
 * Unit	- Department under which the employee work
 * Education	- Rating of Qualification of an employee (1-5)
 * Gender -	Male-0 or Female-1
 * Decision_skill_possess -	Decision skill that an employee possesses
 * Post_Level -	Level of the post in an organization (1-5)
 * Relationship_Status - Categorical Married or Single 
 * Pay_Scale -	Rate in between 1 to 10
 * Time_of_service -	Years in the organization
 * growth_rate	- Growth rate in percentage of an employee
 * Time_since_promotion	- Time in years since the last promotion
 * Work_Life_balance	- Rating for work-life balance given by an employee.
 * Travel_Rate	- Rating based on travel history(1-3)
 * Hometown	- Name of the city
 * Compensation_and_Benefits	- Categorical Variabe
 * VAR1 - VAR5	- Anominised variables
 * Attrition_rate(TARGET VARIABLE)	- Attrition rate of each employee

### Approach: -
 
 * After reading the dataset, step 1 is pre-processing
 * First, I have checked for Missing values data.
 * Missing values are replaced by particular column mean's floor or ceil as per the value of mean
   i.e. if mean = 3.7, then it is 4.0 and if mean = 3.2, then mean = 3.0
 * After this, categorical data are converted into numerical data.
   i.e. Gender = {'M','F'} is changed into Gender = {-1,+1}
 * Some of the categorical data are mapped into numerical using one-hot encoding.
 * After this, association among features is analyzed using statistics(i.e. correlation, mean, q1, q2, q3, ...) and visualization.
 * For visualization, heatmap and pairplot is used to discard correlated features.
 * It is a regression task --- so the candidate models are LinearRegression, Support Vector Regressor, Ridge Regressor and Lasso Regressor
 * Baseline Model for each four candidate is created.
 * SVR has lowest performance on validation data among the four candidate baseline models. So, it is discarded.
 * Two models ridge and lasso are selected for parameter search using validation data as they have comparable performance on validation
   data using their baseline model.
 * A few parameters are searched for both using validation data.
 * Ridge has slight better performace as compare to Lasso, so it is selected for final prediction on test data.
 * Final Ridge model is again trained using trained data and has done prediction on test_data.
 * CSV is created with predicted data.
