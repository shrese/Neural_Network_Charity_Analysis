# Neural_Network_Charity_Analysis

## Overview of the analysis: 

Neural Networks are a powerful machine learning techniques that are modeled after neurons in the brain. They rival robust statistical analytical algorithms without statistical theory. These models are used by large industry leading companies use an advanced form called deep neural networks to analyze images and language processing data sets.
Becs is a data scientist and programmer for the non-profit organization 

AlphabetSoup, an organization dedicated to helping organizations that protect the environment, improve people's wellbeing and unify the world. The organization has raised and donated over $10B in the past 20 years that has been used in life saving technologies and organized reforestation groups around the world.

Becs is in charge of data collection and analysis for AlphabetSoup. She analyzes the impact of each donation and vet potential recipients to ensure that the foundations money is being uses effectively. Unfortunately, not every donation is impactful as some organizations will take the money and run. The company's CEO, Andy Glad, has asked us to predict which organizations are worth donating to and which are too high risk. He is looking for a mathematical data driven solution that will accurately predict risk.

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

image of chart...

The target model performance of 75% or greater was not achieved. It is not certain that it is even possible. To be honest, the steps take to increase the model performance was a guessing game. Each model was adjusted by the input columns, random state, hidden layers, nodes, activation, output layers and epochs to see what would work and what did not work in the model. I found more things that did not work than did. For example, taking out the AFFILIATION and USE_CASE columns made the performance worse by 7.53% when comparing to the original model (AlphabetSoupCharity.ipynb). Also, the more epochs added the worse the performance. The adjustment that seemed to improve the performance, yet marginally, is the number of nodes is the hidden layers and utilizing the RandomForestClassifier model. There was an attempt to utilize the SMV model; however, the model took a very long time to run and was not real efficient.

## Summary: 
OVerfitting?  predictive score? Would more data even work?


Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
