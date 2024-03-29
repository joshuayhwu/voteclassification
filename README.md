# voteclassification

The objective of the exercise is to predict voter turnout for the 2014 general election. 
In other words, the goal of the project is to construct a classifier to predict voter turnout 
for the 2014 general election based on the given data. 

To construct the model, a few assumptions were made. One assumption made is that predicting 
consecutive general elections is more accurate than predicting primary elections in the same year. 
This is informed by the correlations between the general elections. Another assumption made was 
that simpler models are better. This is supported by the lower metric scores 
(precision, recall, and f1) after including additional variables. 

To predict voter turnout for the 2014 general election, a model was trained to predict the 2012 general
election based on the prior assumptions. Across the different algorithms attempted, logistic regression 
has the best overall metric performance. This includes precision, recall, f1-score, and average precision.

A logistic regression model trained with features vh10g, vh08g, and vh12p was found to have the best metrics overall.
Features were selected as the general elections from two previous years and the primary in the same year are 
consistently the three highest features that correlate with the general election in a given year. As a result of 
class imbalance in the data where the majority doesn’t vote, undersampling of the majority class was conducted to 
enhance corresponding metrics scores (precision, recall, f1). Class weight argument was also utilized to help handle 
class imbalance. The F1 score was found to peak at 0.87. 

Consistent with previous years, Europeans and Asians have the highest voter turnout prediction. 
These should be the focused demographics campaign groups. Middle to high-income groups are also 
predicted to have the highest voter turnout, with a focus especially on 125k-200k as well as 200k+. 
Republican and Democratic, have the highest predicted voter turnout. For democrats and republicans, 
voters with turnout are mostly aged 50-70. For non-partisan parties, the age ranges from low 40s to 
mid-60s. Those are the specific demographics campaign groups should focus on.
