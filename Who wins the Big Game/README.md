# Who wins the Big Game?

A sports betting firm has utilized the data augmentation technique to synthesize a data set of championship outcome of the
Big Game's participants and other data. Your task is to generate a model to determine and classify whether a given team will
win the championship or not.

### Data Files
 * train.csv : contains the training data [6500 x 9]
 * test.csv : contains the test data [3500 x 8]
 * sample_submission.csv : example for submission format of Results.csv
 
 ### Data Description
  * ID - A unique identifier for the record
  * Average_Player_Age - Average age of the players on the team
  * Coach_Experience_Level - Level of experience of the head coach
  * Number_Of_First_Round_Draft_Picks - Number of players on the team that were first round draft picks
  * Number_Of_Injured_Players - Number of injured players on the team
  * Number_Of_Wins_This_Season - Number of wins that the team has leading up to the Big Game
  * Playing_Style - Represents playing style in levels
  * Previous_SB_Wins - Number of times the team has won the game in the past
  * Team_Value - Total value of the team in USD [Less than four billion implies greater than 3 billion]
  
  * Won_Championship [Target] - 1 signifies winning the game
                                0 signifies losing the game
                                
### Approach
 * Logistic Regression :
    * feature 'ID' is irrelevant. So It is removed.
    * Hightest Effective feature is ' Number_Of_First_Round_Draft_Picks'.
    * Model is created using Logistic Regression as it is a binary classification problem.
    * One more feature 'Previous_SB_Wins' is removed.
    * Again logistic model is created that gives better classification accuracy as compare to previous model.
    * Result of test.csv are in 'resultV0.5.csv'.
 * SVM : 
    * feature 'ID' is irrelevant. So It is removed.
    * Hightest Effective feature is ' Number_Of_First_Round_Draft_Picks'.
    * Model is created using SVM.
    * k-fold cross validation is used where k=10 to search over a list of features kernel, C and gamma.
    * Best model is selected using GridSearchCV and tested using validation set.
    * Results of test.csv are in 'resultV1.csv'.
    * One more feature 'Previous_SB_Wins' is removed.
    * k-fold cross validation is used where k=10 to search over a list of features kernel, C and gamma.
    * Best model is selected using GridSearchCV and tested using validation set that gives better classification accuracy
      as compare to previous model.
    * Results of test.csv are in 'resultActual.csv'. 
