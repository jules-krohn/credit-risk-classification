# credit-risk-classification


The purpose of this analysis is to see which machine learning module can better predict a healthy or high-risk loan with the given data. The dataset includes data of lending activity from a peer-to-peer lending services company, such as the size of the loan, the interest rate, borrowing income, and whether that loan was a healthy loan or a high-risk loan. The model needed to be able to predict whether or not a loan was high-risk. 
The dataset was comprised of over 77,000 rows, each representing an individual loan. To start the predictive model, the total amount of high-risk loans and healthy loans were counted. There were more healthy loans in the dataset (75,000+ as opposed to ~2,500 high-risk loans). 
The first step in making the predictive model was creating a training dataset and a testing dataset. The training dataset trains the algorithm in the relationships between the type of loan (high-risk or healthy) and the other information provided (borrower income, for example). This training data was then used to test the model, the outputs of which are then compared to the actual data from the original dataset. Training and testing the prediction model is important, because it makes sure that the model can accurately predict data that is already known. If it can, then we can use this model to predict the health of future loans.
After splitting the data into testing and training datasets, it is time to fit the training data to a logistic regression model. Once the data is fit to the model, then next step is to evaluation the model's performance. For this, one can use a balanced accuracy score and a classification report. The balanced accuracy score is average taken of the accuracy in predicting high-risk loans and the accuracy in predicting healthy loans. The classfication report breaks down that accuracy score into healthy and high-risk categories to be able to see the accuracy of each. 

With this particular dataset, the number of healthy loans greatly outweighs the number of high-risk loans. In order to be sure that the model can predict as accurately as possible, having a more evenly dispersed dataset is important. Using the RandomOverSampler model from imblearn, the model randomly selects datapoints from the minority class( high-risk) and adds them to the training dataset. This give the algorithm more data to learn from. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    *The first model without random oversampling had an balanced accuracy score of 95%.
    *Precision of healthy loans: 100%
    *Precision of high-risk loans: 87%
    *Recall score for healthy loans: 99%
    *Recall score for high-risk loans: 91%


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
     *The second model with random oversample had a balanced accuracy score of 99%
     *Precision of healthy loans: 99%
     *Precision of high-risk loans: 99%
     *Recall score for healthy loans: 99%
     *Recall score for high-risk loans: 99%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
The logistic regression model using the resampled data seems to perform the best, as it had a higher precision, accuracy, and recall score across the board. If one is trying to predict healthy loans, either model would work with the same scores; however, predicting high-risk loans with accuracy is less certain, until more data can be acquired. 

