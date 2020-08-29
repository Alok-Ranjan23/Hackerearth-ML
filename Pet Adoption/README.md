### Pet Adoption

#### Problem Statement

A leading pet adoption agency is planning to create a virtual tour experience for their customers showcasing all animals that are available in their shelter. To enable this
tour experience, you are required to build a Machine Learning model that determines type and breed of the animal based on its physical attributes and other factors.

#### Data Description:
The data folder consists of 2 CSV files
* train.csv - 18834 x 11
* test.csv - 8072 x 9

#### Data

Column Description
* pet_id ---> Unique Pet Id
*	issue_date --->	Date on which the pet was issued to the shelter
*	listing_date --->	Date when the pet arrived at the shelter
*	condition --->	Condition of the pet
*	color_type --->	Color of the pet
*	length(m) --->	Length of the pet (in meter)
*	height(cm) --->	Height of the pet (in centimeter)
*	X1,X2 --->	Anonymous columns
*	breed_category --->	Breed category of the pet (target variable)
*	pet_category --->	Category of the pet (target variable)

#### sample_submission(for test file):

* pet_id,breed_category,pet_category
* ANSL_69903,0,1
* ANSL_66892,0,2
* ANSL_69750,2,4
* ANSL_71623,0,2
* ANSL_57969,0,1


#### Evaluation Metric
* s1 = f1_score(actual_values['pet_category'],predicted_values['pet_category'],average = 'weighted')
* s2 = f1_score(actual_values['breed_category'],predicted_values['breed_category'],average = 'weighted')
* score = 100*((s1+s2)/2)
