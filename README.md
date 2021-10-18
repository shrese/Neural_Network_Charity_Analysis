# Neural_Network_Charity_Analysis

## Overview: 

Neural Networks are a powerful machine learning techniques that are modeled after neurons in the brain. They rival robust statistical analytical algorithms without statistical theory. Large industry leading companies use an advanced form called deep neural networks to analyze images and language processing data sets.

Becs is a data scientist and programmer for the non-profit organization 
AlphabetSoup, an organization dedicated to helping organizations that protect the environment, improve people's well-being and unify the world. The organization has raised and donated over $10B in the past 20 years that has been used in life saving technologies and organized reforestation around the world.

She is responsible for data collection and analysis for AlphabetSoup by analyzing the impact of each donation and vet potential recipients to ensure that the foundations money is being uses effectively. Unfortunately, not every donation is impactful; some organizations will take the money and run. The company's CEO, Andy Glad, has asked us to predict which organizations are worth donating to and which are too high risk. He is looking for a mathematical data driven solution that will accurately predict risk.

A decision was made to design and train a deep neural network that will evaluate all types of input data and produces a clear decision-making result.

This will be completed by using the TensorFlow library. This module included learning:
* How neural networks are designed
* Their effectiveness with complex data sets 
* Combine multiple statistical and machine learning models with minimal effort
* Prepare the data for the models
* Create deep learning models
* Design, train, evaluate, and export neural networks

## Results: 
*Data Preprocessing*
* The target for the model is the IS_SUCCESSFUL column which states whether the investment was worthwhile.
* The features are the following columns:
    * APPLICATION_TYPE
    * AFFILIATION
    * CLASSIFICATION
    * USE_CASE
    * ORGANIZATION
    * STATUS
    * INCOME_AMT
    * SPECIAL_CONSIDERATIONS
    * ASK_AMT
* The only columns that should be removed are NAME and EIN.


*Compiling, Training, and Evaluating the Model*  
There were five versions of the model that built on the previous to ensure the optimization of the data.
1. AlphabetSoupCharity.ipynb
2. AlphabetSoupCharity_Optimization.ipynb
3. AlphabetSoupCharity_OptimizationTake2.ipynb
4. AlphabetSoupCharity_Optimization_Forest.ipynb
5. AlphabetSoupCharityOptimizer_SMV.ipynb

![](Resources\chart.PNG)

The target model performance of 75% or greater was not achieved. (It is not certain that it is even possible.) To be honest, the steps take to increase the model performance was a guessing game. Each model was adjusted by the input columns, random state, hidden layers, nodes, activation, output layers and epochs to see what would and would not work in the model. We found more things that did not work than did. For example, taking out the AFFILIATION and USE_CASE columns made the performance worse by 7.53% when comparing to the original model (AlphabetSoupCharity.ipynb). Also, the more epochs added the worse the performance. The adjustment that seemed to improve the performance, yet marginally, is the number of nodes is the hidden layers and utilizing the RandomForestClassifier model. There was an attempt to utilize the SMV model; however, the model took a very long time to run and was not real efficient.

## Summary: 
The predictive score for each model is ~70% giving us the understanding that an accuracy score of 72% is as accurate as the model would be for this data set.  Also, the more data we added, the more it worsened.  The data might be worth splitting into groups or emphasizing on other items that might be more predictive such as the amount of the loan or affiliation.  We could consider other supervised models to see if there is a more accurate way to predict success.

It may even be wise to put the human factor into these decisions rather than taking out the emotions.  Often, having conversations and reviewing the data/applications on a one-on-one basis can be very beneficial for everyone.