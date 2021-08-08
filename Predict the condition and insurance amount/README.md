APPROACH::
### READ THE DATA and Feature Selection:
* IMAGES ARE LESS IN NUMBER. There is clear visual difference between damaged and working vehicle.
* I have used **mahotas** library to evaluate textual features(13 features for an image) of the image.[Paper about textural features](http://haralick.org/journals/TexturalFeatures.pdf) 
* I have removed the missing values.
* I have handled the date column using :: (Current_time - Column_date)
* I have done the feature scaling.
* I have also check for the correlation using **Heatmap** among data columns, and reduced 6 columns as they are highly corrleated to some other features.

### Model Selection for Condition
* I have created SVM and Logisitic Regression baseline and choosen the **SVM** for parameter search.
* I have used **GridSearchCV** to serach the best parameter setting for **SVM** with CV=5.
* I have then trained the whole TRAIN_DATA using the best **SVM model** given by GridSearchCV.
* I have predicted the Condition for TEST_DATA using the best **SVM model** and created the submission file part.

### Model Selection for Amount
* I have created Linear Regression, Lasso, SVR, Ridge, LassoLARS, and BaysianRidge baseline and choosen the **Lasso** for parameter search.
* I have done the serach the best parameter settings for **Lasso** with one-fold approach.
* I have then trained the whole TRAIN_DATA using the best **Lasso model**
* I have predicted the Condition for TEST_DATA using best **Lasso model** and created the submission file's next part.

### Evaluation Metric
##### For predictions of the Condition column
* score1 = max(0, 100*metrics.f1_score(actualConditions, predictedConditions, average="micro"))
##### For predictions of the Amount column
* score2 = max(0, 100*metrics.r2_score(actualAmount, predictedAmount))
##### final_score = (score1/2)+(score2/2)

### Result
* [3rd Rank](https://www.hackerearth.com/challenges/competitive/hackerearth-machine-learning-challenge-vehicle-insurance-claim/leaderboard/predict-the-condition-and-insurance-amount-21-fb647347/)
