# Neural_Network_Charity_Analysis

## Overview

Alphabet Soup is a philanthropic organization that is dedicated to helping other organizations protect the environment, improve the wellbeing of the planet, and unify the world.  Alphabet Soup has been able to raise and donate over $10 billion in the past twenty years.  This money has contributed to building life saving technologies and been used to organize reforestation groups around the world.

The purpose of this project is to ensure that the organization’s money is being used effectively around the world.  Some of the donations have not been impactful as there have been some organizations that have taken the money and disappeared.  The goal is to build a mathematical, data driven solution that can predict which organizations will be worth donating to and which will be too high risk.  We have used a deep learning neural network in order to answer this question.

## Results

Original

Target:
 * IS_SUCCESSFUL

Features:
 * APPLICATION_TYPE
 * AFFILIATION
 * CLASSIFICATION
 * USE_CASE
 * ORGANIZATION
 * STATUS
 * INCOME_AMT
 * SPECIAL_CONSIDERATIONS
 * ASK_AMT

Removed variables (neither targets nor features):
 * EIN
 * NAME

Neurons: (80, 30)
Hidden layers: 2
Activation Functions: Relu, Sigmoid, Sigmoid

Results

![Unoptimized](https://github.com/ForTheGold/Neural_Network_Charity_Analysis/blob/main/Resources/unoptimized.png)

Optimization

Target:
 * IS_SUCCESSFUL

Features:
 * APPLICATION_TYPE
 * AFFILIATION
 * CLASSIFICATION
 * ORGANIZATION
 * STATUS
 * INCOME_AMT

Removed variables (neither targets nor features):
 * EIN
 * NAME
 * SPECIAL_CONSIDERATIONS
 * ASK_AMT
 * USE_CASE

Neurons: (80, 30, 10)
Hidden layers: 3
Activation Functions: Tanh, Sigmoid, Relu, Sigmoid

Results

![Optimized](https://github.com/ForTheGold/Neural_Network_Charity_Analysis/blob/main/Resources/Optimized.png)

The sigmoid and relu functions were selected because of their reputation for high accuracy with low processing power.  The Tanh function was selected by trial and error.  It seemed to produce good results.  The number of layers and neurons was also selected by trial and error as they also produced very good results.

I was unable to produce the desired level of optimization which was 75% despite trying many different things.  I attempted to improve the model by removing noisy variables, changing the activation function, adding layers and neurons, and changing the number of epochs.

## Summary

We were unable to achieve the desired 75% optimization with this model despite having tinkered with it in a variety of ways.  The optimization efforts did not have a significant impact on the model and we got more or less the same results with marginal optimization.

It would also be possible to use logistic regression on this type of a model, and that would be another alternative to try if we are looking for more accurate results.  Logistic regression is used to classify different points into categories.  We could use the model to separate each of the organizations into different categories based on risk.

## Technologies
 * TensorFlow
 * SKLearn
 * Pandas
 * Python
 * Machine Learning
 * Neural Networks
 * Deep Learning