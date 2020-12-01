# Predict the price

### Problem Statement
Halloween is a night of costumes, fun, and candy that takes place every year on October 31. On this day people dress up in various costumes that have a scary overtone and go trick-or-treating to gather candy.

This year, on Halloween, there is a carnival in your neighborhood. Besides the various games, there are also 50 stalls that are selling various products, which fall under various categories.

Your task is to predict the selling price of the products based on the provided features. 


### Data description
The data folder consists of the following three .csv files:
* train.csv: (6368 x 15)
* test.csv: (3430 x 14)
* submission.csv: (5 x 2)

### Column name - Description
* Product_id  - Unique ID of each product
* Stall_no  - Represents the number of stalls in the carnival (1-50)
* instock_date - Represents the date and time on which the product was bought
* Market_Category - Represents the different market categories that the products belong to
* Customer_name - Represents the names of the customers
* Loyalty_customer - Represents if a customer is a loyal customer
* Product_Category - Represents the 10 different product categories that the products belong to
* Grade - Represents the quality of products
* Demand - Represents the demand for the products being sold at the carnival
* Discount_avail - Represents whether a product is being sold at a discount or not
* charges_1 - Represents the types of charges applied on the products in the carnival
* charges_2 (%) - Represents the types of charges applied on the products in the carnival
* Minimum_price - Represents the minimum price of a product
* Maximum_price - Represents the maximum price of a product
* Selling_Price - Represents the selling price of the product in the carnival[target]


### Evaluation metric

* score = max(0,100 - RMSLE(actual\_values,predicted\_values))
