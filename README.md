# UCI_Rainfall_Predict

The Problem
Our competition data are satellite-based measurements of cloud temperature (infrared imaging),
being used to predict the presence or absence of rainfall at a particular location.
The data are courtesy of the UC Irvine Center for Hydrometeorology and Remote Sensing,
and have been pre-processed to extract features corresponding to a model they use actively for predicting rainfall across the globe.
Each data point corresponds to a particular lat-long location where the model thinks there might be rain;
the extracted features include information such as IR temperature at that location, and information about the corresponding cloud
(area, average temperature, etc.). The target value is a binary indicator of whether there was rain (measured by radar) at that location;
you will notice that the data are slightly imbalanced (positives make up about 30% of the training data).

The Evaluation
Scoring of predictions is done using AUC (Links to an external site.)Links to an external site.,
the area under the ROC (receiver-operator characteristic) curve. 
This gives an average of your learner’s performance at various levels of sensitivity to positive data.
This means that you will likely do better if, instead of simply predicting the target class, you also include your confidence level 
of that class value, so that the ROC curve can be evaluated at different levels of specificity. To do so, you can report your confidence
that it is raining (class +1) as a real number for each test point. Your predictions will then be sorted in order of confidence,
and the ROC curve evaluated.
