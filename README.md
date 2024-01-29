# deep-learning-challenge
Week 21 - Neural Networks

### Analysis Overview: 
The purpose of this analysis was to create a binary classifier that can predict whether applicants will be successful if funded by a certain company, Alphabet Soup. The goal was to attain an end accuracy result of over 75% using Kera's model with tensorflow, which was achieved

### Results: 

Data Preprocessing

##### What variable(s) are the target(s) for your model?
- the target variable was 'IS_SUCCESSFUL' which referred to whether the money was used successfully by the applicant after being funded

###### What variable(s) are the features for your model?
- The features were the categorical columns whose datatypes were 'object', containing non-numerical rows of data which were converted into numerical values using ```pd.get_dummies()```, the pre-dummified columns listed in the following:
  ```
  'APPLICATION_TYPE',
  'AFFILIATION',
  'CLASSIFICATION',
  'USE_CASE',
  'ORGANIZATION',
  'INCOME_AMT',
  'SPECIAL_CONSIDERATIONS'
  ```
##### What variable(s) should be removed from the input data because they are neither targets nor features?
All remaining columns with numerical data which were: ```ASK_AMT,STATUS```

##### How many neurons, layers, and activation functions did you select for your neural network model, and why?
I selected 2 hidden layers, with the following neurons: 10 and 15 respectively. Both hidden layers had 'relu' activation's, except the output layer which was a 'sigmoid' activation. This is due to the binary nature of what we are trying to produce with the neural network model, meaning output will only be 1. 

##### Were you able to achieve the target model performance?
Yes

##### What steps did you take in your attempts to increase model performance?
I revisited my dummy data, ensured the features count was correct and corresponding to the number of unique values of each column getting processed in .get_dummy(). I also adjusted the number of neurons to 10 and 15 per layer. 

### Summary:
The results of the model creates insight into understanding how the hyperparameters affect the training of the model with the given data, and one run of training the model will not always suffice. My recommendation would be to trial and error with neurons and hidden layers, and if you run into troubleshooting issues, revisit you input data (typically the converted features, dummy data) and utilize the built-in functions to view the create features such as ```dummy.shape[1]``` which will give you the number of features, or to troubleshoot deeper, ```dummy.columns``` to view each feature created.
