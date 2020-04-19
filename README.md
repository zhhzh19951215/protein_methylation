# Protein_methylation
## We compare the performance of three learning methods.
****
## Dataset
### Our training set has 19988 data sets and our test data set has 4996 data sets. Each data has 29 features. These features extracted using ProtDCal (doi:10.1002/pro.3673).
****
## Data pre-processing
### 1.Remove outliers using zscore method
### 2.For Bayesian belief network and DNN, we normalized the data.
### 3.There is a serious data imbalance in the data set. So we take the upsampling method for the positive data.
****
## Classifier
### Naive Bayes classifier & Decision tree
#### Naive Bayes classifiers require features to be directly independent. So we calculate the correlation between features(redundancy) and delete the features with high correlation.
#### Calculate correlation between remaining features and label. Then we calculate the value of (relavance-redundancy) and sorted features by this value.
### DNN
#### First, we used grid search to determine the network structure. Then, we train on the training set and use the validation set to observe the performance.

