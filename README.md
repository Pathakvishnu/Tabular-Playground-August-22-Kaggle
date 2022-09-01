# Tabular-Playground-August-22-Kaggle

## Description 
The August 2022 edition of the Tabular Playground Series is an opportunity to help the fictional company Keep It Dry improve its main product Super Soaker. The product is used in factories to absorb spills and leaks.

The company has just completed a large testing study for different product prototypes. Can you use this data to build a model that predicts product failures?

![image](https://user-images.githubusercontent.com/37989419/187835445-78557d79-da03-4a73-86b9-c1a92d43f34a.png)

## Evaluation Criteria 
The model are evaluated on area under the ROC curve between the predicted probability and the observed target.

## Learning 
Although this was a kaggle playgroud challenge but it will give you same fun and challenge experience as competition problem.
**NOTE** : There was a trap of overfitting in public leaderboard.
> **Feature Selection is important**:
Given 25 features if you use all the 25 features for predicting the failure there's 100% chance you going to overfit the data. As not all features were contributing towards the prediction of failure i.e. there is no relationship. Most of the measurement features is irrelavant except measurement_0,
measurement_1,measurement_2,measurement_17. Now question is how to validate which features is important? Answer lies in the concept of **Adversarial Validation** technique. To know about this technique visit this [link](https://www.kaggle.com/code/carlmcbrideellis/what-is-adversarial-validation/notebook)

> **Missing value imputation**:
There were quite a lot of missing values especially in measurement features. A simple mean imputation does not give good OOF score. But, there is a get technique applied for imputaion mentioned in the my notebook. It uses a mix of KNN imputation and Robust linear regression to fill up the missing values. Credit to this [kaggler](https://www.kaggle.com/code/pourchot/hunting-for-missing-values) who had come up with this idea.

>**Trust your cross-validation**:
In kaggle, I have observed that if you trust your cross-validation score you will have good private leaderboard result. Many of us just go with the emotion of high score in public leaderboard & overfit our model.


## Achievment
My private leaderboard rank in this competition is 28.
