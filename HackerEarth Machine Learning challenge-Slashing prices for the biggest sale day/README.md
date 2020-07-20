### Predict the lowest price

A leading global leader of e-commerce has over 150 million paid subscription users. One of the many perks of the subscription is the privilege of buying products 
at lower prices. For an upcoming sale, the organization has decided to promote local artisans and their products, to help them through these tough times. However, 
slashed prices may impact local artists.
To not let discounts affect local artists, the company has decided to determine the lowest price at which a particular good can be sold. Your task is to build a predictive
model using Machine Learning that helps them set up a lowest-pricing model for these products.
You have to predict the Low_Cap_Price column.

Project : [link](https://www.hackerearth.com/challenges/competitive/hackerearth-machine-learning-challenge-predict-the-lowest-price/)

### Data 
##### Data description

 * Item_Id	- Unique item ID
 * Date -	Date
 * State_of_Country	- State no. of the country
 * Market_Category	- Category of the market to which the product belongs to
 * Product_Category	- Category of the product
 * Grade -	Quality of the product
 * Demand -	Demand rate of the product in the market
 * Low_Cap_Price [Target]	- Lowest price that can be offered 
 * High_Cap_Price	- Original maximum price in the current market

##### Data files
The dataset folder consists of the following files:
 * Train.csv: Contains training data [9798 x 9] that must be used to build the model
 * Test.csv: Contains test data [5763 x 8] to be predicted on
 * sample_submission.csv: Contains sample submission format with dummy values filled for test data 
 
##### Evaluation metric
 * score = max(0,(100-mean_squared_log_error(actual_values,predicted_values))) 
 
##### Approch

1. Pre-processing
 * Date column is formatted and normalized.
 * Redundant Id column is removed.
 * Validation set is created. (25%--validation and 75% --- training)
2. Feature Selection
 * All features are selected after pre-processing.
3. Model Selection
 * Baseline for Linear Model, SVR, Lasso, Ridge and MLP is created.
 * Choosen model is MLP.
4. Prediction on Actual test data 
 * An MLP model with 11 layers is created.
 * The whole train_data is used for training with validation split set as 0.25.
 * Validation loss(mean_squared_logarithmic_error) is monitored. 
 * Weights for best loss is stored.
 * Best weights are used to get the prediction for test_data and submission.csv is created as specified.
 * Stored
