# Kaggle_Higgs_bosson
End semester project

Abstract 

The goal of the challenge presented by this kaggle data set is to find a region in feature space, in which there is a significant excess of signals corresponding to the Higgs Boson signal. We have used two types of ensemble models - Random Forests and Adaboost. 
Random forest with OOB instead of cross validation has been chosen since it is faster and better with large dataset. Combining bagging with random forest will solve the problem of one feature dominating due to decorelation created by random forest.(as random forest will choose sqr(p) features randomly to split).
We chose Adaboost because we wanted to experiment with different learning rates. Adaboost is not prone to overfitting and we slightly overfit random forest to get better accuracy hence Adaboost would be a good model to compare with the Random forest model.
We chose F1_score to measure the performance of the model.
