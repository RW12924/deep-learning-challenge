# deep-learning-challenge

## Overview
The purpose of this analysis was to produce a neural network model that would predict the success or failure of business applicants to the Alphabet Soup foundation.
The model was trained using data on over 34,000 organizations that previously received funding from Alphabet Soup.

## Results

### Data Preprocessing
- The main target for this model was the "IS_SUCCESSFUL" column in the data set.  This column confirmed whether or not the applicants were successful and if the
money provided to them was used effectively.

- The features used for this model were Application Type, Affiliation, Classification, Use Case, Organization, Status, Income Amount, Special Considerations,
and Ask Amount.

- The variables that were removed from the input data were the EIN and Name columns.  These columns were neither targets nor features because they were only used
to identify applicants.

### Compiling, Training, and Evaluating the Model
- In the initial model, a total of 13 neurons across two hidden layers were used.  In the optimized model, a total of 18 neurons accross three hidden layers were used. Additional neurons and layers were included to improve the accuracy of the model.

- Two different activation functions were used in the model: ReLU and Sigmoid.  ReLU was used for the hidden layers due to its high effectiveness in a wide variety of scenarios.  Sigmoid was used in the output layer because the majority of our data was binary (0 or 1) which is what sigmoid activation excels with.

- In addition to increasing the number of hidden layers and neurons, several other optimization steps were used.  The steps taken include increasing the number of values for the Application Type bin, increasing the number of values for the Classification bin, and increasing the number of epochs used when training the model.

- The optimization steps taken were insufficient to achieve the target model performance of 75%.

## Summary
- In the optimized version of the model, we received a loss value of 0.5706 and a accuracy value of 0.7237.  The loss value indicates that on average, the difference between the model's predictions and the actual probabilities was 0.5706.  The accuracy indicates that 72.37% of the model's predictions were correct.

- The accuracy of this model is less than the targeted 75% so an alternative model with a higher accuracy rating would be preferred.  In the alternative model, it may be helpful to remove the Ask Amount column from the training data set.  With so many unique values in the column, it seems to resemble a regression problem more than the classification problem we have at hand.