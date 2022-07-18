# Kaggle_Higgs_bosson (End semester project)
In search of Higgs Boson signal within the data generated by LHC at CERN. Data is publically available on kaggle(https://www.kaggle.com/c/higgs-boson)

Project is Presented within 3 Jupyter Notebooks as follows 
Notebook 1: Pre-processing and cleaning of the data, Exploratory Data Analysis, Base Model
Notebook 2: Ensemble Model_1: Random Forest, SMOTE: Data Upsampling
Notebook 3: Ensemble Model_2: Adaboost, SMOTE: Data Upsampling, Conclusion


Abstract 

The goal of the challenge presented by this kaggle data set is to find a region in feature space, in which there is a significant excess of signals corresponding to the Higgs Boson signal. We have used two types of ensemble models - Random Forests and Adaboost. 
Random forest with OOB instead of cross validation has been chosen since it is faster and better with large dataset. Combining bagging with random forest will solve the problem of one feature dominating due to decorelation created by random forest.(as random forest will choose sqr(p) features randomly to split).
We chose Adaboost because we wanted to experiment with different learning rates. Adaboost is not prone to overfitting and we slightly overfit random forest to get better accuracy hence Adaboost would be a good model to compare with the Random forest model.
We chose F1_score to measure the performance of the model.


Table of contents

1.1 About the data
1.2 About LHC detector and Analysis Pipeline
2 Features
3.1 Notebook 1: Pre-processing and cleaning of the data, Exploratory Data Analysis, Base Model
3.2 Notebook 2: Ensemble Model: Random Forest, SMOTE: Data Upsampling
3.3 Notebook 3: Ensemble Model: Adaboost, SMOTE: Data Upsampling, Conclusion
F 4uture Enhancements
4 References


1.1 About the Data
Data documentation 
Understanding the problem statement:
Higgs boson is an elementary particle in the Standard Model of particle physics.  It is also very unstable, decaying into other particles almost immediately.
In this kaggle data set we work with Higgs bosons decay into tau-tau. 

1.2 About LHC detector and Analysis Pipeline
When proton-proton collisions happen in LHC, it is called an Event.
Hundreds of particles resulting from an Event are detected by sensors. Raw data is collected for these particles (energy, type, 3D-direction). This information is copied by a large CPU farm. Background processes are decays of previously discovered particles. The Events saved by the CPU farm majorly have background processes.
Goal of Analysis is to find a region in feature space, in which there is significant excess of signals corresponding to Higgs Boson signal. And the goal of the Kaggle challenge is to improve the procedure that produces the selection region.

2 Features
The variables prefixed with PRI (primitive) are quantities about the collisions as measured by the detector, essentially momenta of the particles. Variables prefixed with DER (derived) are quantities computed from primitive features(using fundamental equations of special relativity). The target variable is the label with values as signal(signal for Higgs Boson) or background. 
Whenever the calculated quantities are undefined or cannot be computed in this case their value is -999, which is outside the normal range of all variables.
