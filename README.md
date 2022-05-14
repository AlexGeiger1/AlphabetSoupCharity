# AlphabetSoupCharity
## Objective 
### Purpose
The purpose of the analysis was to predict whether applicants will be successful if funded by AlphabetSoup using Neural Networks.

## Results
### Data Processing
- The target variable is "IS_SUCCESSFUL" which indicates if funding was successful.
- The features of the model include; 
  - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
![Application DataFrame](https://github.com/AlexGeiger1/AlphabetSoupCharity/blob/main/Resources/datframe.png)
- The feature that was dropped
  - EIN: Employee Identification Number
  - NAME (was initially removed but re-added during the optimization phase)
### Compiling, Training, and Evaluating the Model
- 2 Hidden layers, First layer had 80 neurons, Second layer had 30 neurons. "ReLu" activation function was used for the input layers and Sigmoid was used for the output layers
- The initial accuracy was 72% but after optimization accuracy reached 78% which is above the target model performance.
- Dropping fewer columns and binning on NAME, the target model performance was achieved. 
## Summary

### Conclusion
Initially, it was found that the features only results in a 72% accuracy, which is below the targeted model performance. However, after trying to change the number neurons and number of epochs didn't work, attempting to use NAME for binning brought the accuracy up to 78%. 

### Recomendation for Different Model
I recommend using the RandomForest Model because it do better with the categorical variables. 
