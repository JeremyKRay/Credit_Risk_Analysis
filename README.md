# Credit_Risk_Analysis
## Overview of the Analysis
The purpose of this analysis was to compare several different machine learning models to determine which is best at predicting credit card risk. The dataset used came from LendingClub, a peer-to-peer lending services company. Credit risk is an inherently unbalanced classification problem. Good loans greatly outnumber risky loans. This is why we are using 6 different machine learning techniques to train and evaluate models with unbalanced classes. The techniques fall under 4 different categories and are imported from the imbalanced-learn library. Under oversampling, we employ RandomOverSampler and SMOTE algorithms. Under undersampling we employ the ClusterCentroids algorithm. We use a combination of the over and undersampling techniques by employing the SMOTEENN algorithm. And finally, under Ensemble learning techniques we employ BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms. These last two are fairly new and reduce bias. To compare all of the techniques, the scikit-learn library is used to produce a balanced acuracy score and precision and recall scores to determine if they are suitable techniques at predicting credit risk. 
 
## Results
Below, I have listed each of the machine learning techniques under their respective categories. For each, I have included a snap shot of the balanced accuracy score and the precision and recall scores. These are 3 ways of measuring a model's performance. Below the snap shot, I have included a brief analysis. The accuracy score is simply the percentage of predictions that are correct. An accuracy score is not always an appropriate or a meaningful performance metric, however.  in machine learning, precision is a measure of how reliable a positive classification is. Recall is a measure of how likely it is that a positive classification was made when appropriate.     

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
	
![EasyEnsemble.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/e01eeeb6ae6c0620df361d0f4c19f7b1ae0c68ed/Module-17-Challenge-Resources/Images/EasyEnsemble.png)

## Summary

Summary of results:
Below is a summary table of the results:

![summary.png](https://github.com/JeremyKRay/Credit_Risk_Analysis/blob/91b25012196dc096c59572969ef4b1c87f44ddcc/Module-17-Challenge-Resources/Images/Summary.png)

My recommendation would be to use either of the newer machine learning models, BalancedRandomForestClassifier or EasyEnsembleClassifier. They both have the higher accuracies and also a good balance between Precision and Recall or Sensitivity, high F1 scores. 
