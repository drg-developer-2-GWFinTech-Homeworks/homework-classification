# Unit 11—Risky Business

<style>
    body {background-color: green;}
    h1   {color: blue;}
    p    {color: red;}
    .center {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 50%;
}

</style>
<img src="Images/credit-risk.jpg" alt="Paris" class="center" width="400">

## Background

Auto loans, mortgages, student loans, debt consolidation ... these are just a few examples of credit and loans that people are seeking online. Peer-to-peer lending services such as LendingClub or Prosper allow investors to loan other people money without the use of a bank. However, investors always want to mitigate risk, so you have been asked by a client to help them use machine learning techniques to predict credit risk.

In this assignment, machine-learning models are built and evaluated to predict credit risk using free data from LendingClub. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so different techniques will need to be used for training and evaluating models with imbalanced classes.

Two classes of models will be used:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

## Resampling Procedure

The [imbalanced learn](https://imbalanced-learn.readthedocs.io) library will be used to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data.

The procedure will involve:

1. Load the Lending Club data, split the data into training and testing sets, and scale the features data.
2. Oversample the data using the `Naive Random Oversampler` and `SMOTE` algorithms.
3. Undersample the data using the `Cluster Centroids` algorithm.
4. Over- and under-sample using a combination `SMOTEENN` algorithm.

For each of the above:

1. Train a `logistic regression classifier` from `sklearn.linear_model` using the resampled data.
2. Calculate the `balanced accuracy score` from `sklearn.metrics`.
3. Calculate the `confusion matrix` from `sklearn.metrics`.
4. Print the `imbalanced classification report` from `imblearn.metrics`.

## Ensemble Learning Procedure

In this section, two different ensemble classifiers will be trained and compared to predict loan risk and evaluate each model. The [Balanced Random Forest Classifier](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.ensemble.BalancedRandomForestClassifier.html#imblearn-ensemble-balancedrandomforestclassifier) and the [Easy Ensemble Classifier](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.ensemble.EasyEnsembleClassifier.html#imblearn-ensemble-easyensembleclassifier) will be used.

The following procedure will be used:

1. Load the Lending Club data, split the data into training and testing sets, and scale the features data.
2. Train the model using the quarterly data from LendingClub provided in the `Resource` folder.
3. Calculate the balanced accuracy score from `sklearn.metrics`.
4. Print the confusion matrix from `sklearn.metrics`.
5. Generate a classification report using the `imbalanced_classification_report` from imbalanced learn.
6. For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.

## Conclusions

### Resampling Models Conclusions

> Which model had the best balanced accuracy score?



> Which model had the best recall score?

> Which model had the best geometric mean score?

### Ensemble Learning Models Conclusions

> Which model had the best balanced accuracy score?

> Which model had the best recall score?

> Which model had the best geometric mean score?

> What are the top three features?
