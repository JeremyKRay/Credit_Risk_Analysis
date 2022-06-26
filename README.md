# Credit_Risk_Analysis
## Overview of the Analysis
The purpose of this analysis was to compare several different machine learning models to determine which is best at predicting credit card risk. The dataset used came from LendingClub, a peer-to-peer lending services company. Credit risk is an inherently unbalanced classification problem. Good loans greatly outnumber risky loans. This is why we are using 6 different machine learning techniques to train and evaluate models with unbalanced classes. The techniques fall under 4 different categories and are imported from the imbalanced-learn library. Under oversampling, we employ RandomOverSampler and SMOTE algorithms. Under undersampling we employ the ClusterCentroids algorithm. We use a combination of the over and undersampling techniques by employing the SMOTEENN algorithm. And finally, under Ensemble learning techniques we employ BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms. These last two are fairly new and reduce bias. The scikit-learn library is used to test and train the models and to compare all of the techniques, producing a balanced acuracy score and precision and recall scores to determine if they are suitable techniques at predicting credit risk. 
 
## Results
Below, I have listed each of the machine learning techniques under their respective categories. For each, I have included a snap shot of the balanced accuracy score, precision and recall scores. These are 3 ways of measuring a model's performance. The accuracy score is simply a percentage of predictions that are correct, or how likely, no matter the outcome, is the model going to be correct. An accuracy score is not always an appropriate or a meaningful performance metric, however. In machine learning, precision is included as a measure of how reliable a positive classification is. In other words, I know that the test identified a person as a credit risk. How likely is it that they are in fact a credit risk? In addition, recall or sensitivty a measure of the percentage of people who actually are a credit risk are correctly identified. With this project, we are dealing with predicting credit risk. So, we ask the question, is it more important that the model is simply predicting the correct outcome of credit risk (accuracy) or that the model is predicting a person as a credit risk and they that are in fact a risk (precision) or that credit risk is predicted where it in fact exists (recall)? This is not a simple question to answer, and what we really want is a good balance between precision and recall and in general a high accuracy score, 75% or more.

### Oversampling

	1) RandomOverSampler
	
![RandomOverSampler.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/a20f0c9bbf2087bf09ce2fc22aded860f85d88b2/Module-17-Challenge-Resources/Images/RandomOverSampler.png)

	2) SMOTE
	
![SMOTE.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/17122c17ace751bb63bccd62a119288cfce57213/Module-17-Challenge-Resources/Images/SMOTE.png)

### Undersampling

	3) ClusterCentroids

![ClusterCentroids.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/4c1cfdaece3460cfab392bdf2b0eb629b2408b48/Module-17-Challenge-Resources/Images/ClusterCentroids.png)

### Combination

	4) SMOTEENN

![SMOTEEN.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/9cd085999ab7ff720884f922cfc8be1856737492/Module-17-Challenge-Resources/Images/SMOTEENN.png)

### Ensemble Learners

	5) BalancedRandomForestClassifier
	
![BalancedRandomForestClassifier.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/44dcb08c0d7396d70e3194e05d30e6c58d10cc08/Module-17-Challenge-Resources/Images/BalancedRandomForestClassifier.png)
	
	6) EasyEnsemmbleClassifier
	
![EasyEnsemble.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/5271adfcbb944922ce68b6f6dc5513b80a346a14/Module-17-Challenge-Resources/Images/EasyEnsemble.png)

## Summary

Summary of results:
Below is a summary table of the results:

![summary.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/54f0ab90d3877df455a64d94ece9b21d1a5821ae/Module-17-Challenge-Resources/Images/Summary.png)

As you can see precision is 99% across the board, so this metric is not all that helpful on its own. By including the F1 score, however, it can still be included in our analysis of the techniques. The F1 score is a measure of the balance between precision and recall. The lower the score, the further a part they are or the less balance there is between the two. The lowest scores for accuracy occur when oversampling and undersampling techniques are used alone and only slightly improves with the combination technique SMOTEEN. Recall and F1 score is lowest with the undersampling technique, ClusterCentroids. And oversampling actually out performs SMOTEEN in Recall and F1. The best performers by far are the newer machine learning Ensemble techniques, with EasyEnsembleClassifier out performing them all with a 92.54% accuracy score, 99% Precision score, 94% Recall score, and 97% F1 score.

My recommendation would be to use either of the newer machine learning model EasyEnsembleClassifier. BalancedRandomForestClassifier seems to be a suitable technique as well, but with an accuracy score of 78.78%, it just falls a little short. This is a decent score, but EasyEnsemble comes in at 92.54% so I would recommend this technique. 
