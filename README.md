# Neural_Network_Charity_Analysis

## Overview
The purpose of this project is to create a deep neural network model that will predict which applicants Alphabet Soup should invest in. We have data of more than 34,000 organizations and their applications. Our model will act as a binary classifier to help identify which applicants will be the most successful and worthy of funding. 
Application information includes identification columns, application type, their affiliated industries, government organization classification, the use for the funding, organization status, income classification, any special considerations for their application, the requested funding amount, and whether or not th e money was used effectively. 

## Results
### Data Preprocessing
* The target for our model is the 'is successful' variable. It tells us if the money was used effectively by the organization.
* The features are application type, affiliation, classification, use case, organization, status, income amount, special considerations, and ask amount. 
* The unique identifying variables such as EIN and Name should be removed from the input data. They are not targets or features that would help the model as they are all unique data points that do not have anything to do with success/failure of funding.

### Compiling, Training, and Evaluating the Model
![Capture1](https://user-images.githubusercontent.com/100896787/183796601-611fbb8f-d11c-40a0-802a-0bfd0190e45b.PNG)
* In our optimized model, we have two hidden layers that use 8 and 5 neurons. 

![Capture2](https://user-images.githubusercontent.com/100896787/183796611-a0d641b4-a317-4eae-b0b9-069a1367f821.PNG)
![Capture3](https://user-images.githubusercontent.com/100896787/183796617-1838b999-718d-4091-af2d-ad0dcde2b020.PNG)
* After more data preprocessing, we were able to achieve a target model performance of 82.35% (a big achievement from the previous 18.60%).

![Capture4](https://user-images.githubusercontent.com/100896787/183796660-0dfa285f-fee6-4045-9b73-fa0fa9bece86.PNG)
* To increase model performance, we looked again at the features. Noticing that the ask amounts were showing 8,747 unique values, I binned the values into groups of 5k, 5-10k, 10-25k, 25-50k, 50-100k, 100-500k, 500k-1M, 1M-5M, and over 5M. By doing so, we reduced the unique values down to 9. We kept all the other preprocessing procedures from the original model, as well as the neuonsz, layers, and activation functions and saw that we were able to increase our accuracy rate above the required 75%. 

## Summary
After doing more steps by eliminating the number of unique values in the ask amount, we were able to make the model more efficient. If we were to try using a logistic regression model, we wouldn't need to preprocess or scale the data, which would save more time. However, there is a possibility that our dataset may be too big, which is where a neural network model may have the advantage. It would still be worth a shot to test and compare. 
