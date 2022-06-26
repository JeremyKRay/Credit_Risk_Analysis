# Credit_Risk_Analysis
## Overview of the Analysis
The purpose of this analysis was to compare several different machine learning models to determine which is best at predicting credit card risk. The dataset used came from LendingClub, a peer-to-peer lending services company. Credit risk is an inherently unbalanced classification problem. Good loans greatly outnumber risky loans. This is why we are using 6 different machine learning techniques to train and evaluate models with unbalanced classes. The techniques fall under 4 different categories and are imported from the imbalanced-learn library. Under oversampling, we employ RandomOverSampler and SMOTE algorithms. Under undersampling we employ the ClusterCentroids algorithm. We use a combination of the over and undersampling techniques by employing the SMOTEENN algorithm. And finally, under Ensemble learning techniques we employ BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms. These last two are fairly new and reduce bias. To compare all of the techniques, the scikit-learn library is used to produce a balanced acuracy score and precision and recall scores to determine if they are suitable techniques at predicting credit risk. 
 
## Results
Below, I have listed each of the machine learning techniques under their respective categories. For each, I have included a snap shot of the balanced accuracy score and the precision and recall scores. These are 3 ways of measuring a model's performance. Below the snap shot, I have included a brief analysis. The accuracy score is simply the percentage of predictions that are correct. An accuracy score is not always an appropriate or a meaningful performance metric, however.  in machine learning, precision is a measure of how reliable a positive classification is. Recall is a measure of how likely it is that a positive classification was made when appropriate.     

Oversampling
	* RandomOverSampler
	* SMOTE
Undersampling
	* ClusterCentroids
Combination
	* SMOTEENN
Ensemble Learners	
	* BalancedRandomForestClassifier
	* EasyEnsemmbleClassifier
## Summary

Summary of results:

Recommendation of which model to use, or if there is no recommendation, justify.
