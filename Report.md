# Report Deep Learning Challenge

## Overview 

The nonprofit foundation Alphabet Soup aims to develop a tool that helps select funding applicants with the best chance of succeeding in their ventures. This report presents the results of a binary classifier designed to predict whether applicants will be successful if funded by Alphabet Soup. These models were created using machine learning and neural networks, based on a CSV dataset containing information about over 34,000 organizations that have received funding from Alphabet Soup over the years.

## Data and data preprocessing

TThe Alphabet Soup Foundation provided a CSV file containing data on approximately 34,000 organizations that received funding. The CSV includes the following columns as features:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special considerations for application
* ASK_AMT—Funding amount requested

The column that was used as target variable (y) was: IS_SUCCESSFUL, which contains the results about money used effectively.

Key preprocessing steps included:

1. Dropping the EIN and NAME columns.
2. Reducing the unique values of the APPLICATION_TYPE and CLASSIFICATION columns. Rare categories were grouped into an "Other" category based on a defined threshold.

## Results - Compiling, Training, and Evaluating the Model

Two models were created:

### First Model

Summary of the first model:
| Layer  | Output Shape | Params |
| ------ | ------------ | -------|
| Dense  | (None, 80)   | 3,520  |
| dense_1| (None, 30)   | 2,430  |
| dense_2| (None, 1 )   | 31     |

After training the model using the preprocessed and cleaned data, it achieved an accuracy of 0.7290 and a loss of 0.5681 over 100 epochs.

This indicates that the model can explain approximately 72.90% of the data.

### Second Model (Optimization)

Summary of the second model:
| Layer  | Output Shape | Params |
| ------ | ------------ | -------|
|dense_3 | (None, 90)   | 3,960  |
| dense_4| (None, 40)   | 3,640  |
| dense_5| (None, 20)   |   820  |
| dense_6| (None, 1 )   | 21     |

After training this model using the same preprocessed and cleaned data, it achieved an accuracy of 0.7262 and a loss of 0.5902 over 150 epochs.

This slight improvement in accuracy (72.62%) demonstrates that the second model, which included an additional layer and more neurons, did not significantly outperform the first model. Despite utilizing more resources, it produced nearly identical results.


### Third Model (Optimization)

Summary of the third model:
| Layer  | Output Shape | Params |
| ------ | ------------ | -------|
| dense_7| (None, 80)   | 3,840  |
| dense_8| (None, 30)   | 2,430  |
| dense_9| (None, 1 )   | 31     |

This model used bins to organize data of the ASK_AMT variable, which contained the data about the quantity of money asked to the organization for their projects. After training the model, it achieved an accuracy of 0.7294 and a loss of 0.5680 over 150 epochs.

This indicates that the model can explain approximately 72.94% of the data. This model produced identical results as the first model.

### Fourth Model (Optimization)

Summary of the fourth model:
| Layer  | Output Shape | Params |
| ------ | ------------ | -------|
|dense_10| (None, 80)   | 3,440  |
|dense_11| (None, 30)   | 2,430  |
|dense_12| (None, 1 )   | 31     |

After training this model using the same preprocessed and cleaned data (dropping variable ASK_AMT), it achieved an accuracy of 0.7287 and a loss of 0.5714 over 150 epochs.

This model shows slight improvement in accuracy (72.87%) in comparison with the second and third model of optimization.

## Summary and Conclusions

1. Although the dataset contained a large number of observations, additional data may be necessary for further analysis. Having access to historical data could also provide insights into the long-term success of funded organizations.

2. The first model explained the majority of the target variable's outcomes (72.9%) without overfitting, indicating that it is a reliable model.

3. The optimized models, despite being more complex and requiring greater computational resources, offered no significant improvement over the first model. This underscores the importance of optimizing models to achieve the best results using fewer resources.

In conclusion, the first model appears to be the better choice as it balances simplicity and performance effectively.



