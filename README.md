# Credit_Risk_Analysis
## Overview of the Analysis
The purpose of this analysis was to compare several different machine learning models to determine which is best at predicting credit card risk. The dataset used came from LendingClub, a peer-to-peer lending services company. Credit risk is an inherently unbalanced classification problem. Good loans greatly outnumber risky loans. This is why we are using 6 different machine learning techniques to train and evaluate models with unbalanced classes. The techniques fall under 4 different categories and are imported from the imbalanced-learn library. Under oversampling, we employ RandomOverSampler and SMOTE algorithms. Under undersampling we employ the ClusterCentroids algorithm. We use a combination of the over and undersampling techniques by employing the SMOTEENN algorithm. And finally, under Ensemble learning techniques we employ BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms. These last two are fairly new and reduce bias. To compare all of the techniques, the scikit-learn library is used to produce a balanced acuracy score and precision and recall scores to determine if they are suitable techniques at predicting credit risk. 
 
## Results
Below, I have listed each of the machine learning techniques under their respective categories. For each, I have included a snap shot of the balanced accuracy score, precision and recall scores. These are 3 ways of measuring a model's performance. The accuracy score is simply percentage of predictions that are correct, or how likely, no matter the outcome, is the model going to be correct. An accuracy score is not always an appropriate or a meaningful performance metric, however. In machine learning, precision is included as a measure of how reliable a positive classification is. In additionm, recall or sensitivty is a measure of how likely it is that a positive classification was actually made when it was supposed to have been. With this project, we are dealing with predicting credit risk. So, is it more important that the model is simply predicting the correct outcome of credit risk (accuracy) or that the model is correctly predicting credit risk customers are infact risky (precision) or that credit risk is predicted where it exists. What we really want is a balance between precision and sensitivity or recall and in general a high accuracy score, 75% or more.

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

As you can see 
My recommendation would be to use either of the newer machine learning models, BalancedRandomForestClassifier or EasyEnsembleClassifier. They both have the higher accuracies and also a good balance between Precision and Recall or Sensitivity, high F1 scores. 
