# Loan Default Classification - DTSA 5009

## Project Overview 
Final project from a Supervised Machine Learning class to binary classify loans into default and non-default. Project compared decision tree, pruned decision tree, and the ensemble methods AdaBoost and Random Forest.

## Data Source
Data was sourced from [Kaggle](https://www.kaggle.com/datasets/nikhil1e9/loan-default) which was taken from Coursera's Loan Default Prediction Challenge.

Data includes 225,000+ samples with 18 features including continous (age, income, loan amount), categorical variables (employment status, marital status) and boolean variables (has dependents). Data types were modified and others removed prior to modeling. Default labeling was quite biased (only 11.6% of samples were labeled for default) which was accomodated by weighting default points more heavily. Features were then evaluated for correlation with default, revealing strong negative correlation with age and and positive correlation with loan amount and interest rate. There was no significant colinearity between features.

## Models
The intent of the project was to compare the various decision tree methods' performance on accuracy of classification. The test models included:
* Unpruned Decision Tree
* Pruned Decision Tree - remedies overfitting issues.
* AdaBoost (stumps, up to 100 learners)
* AdaBoost - Feature engineered to top 5 features
* Random Forest (stumps, up to 200 learners)
* Random Forest (depth 5, up to 200 learners)

## Conclusion
The analysis indicated the pruned decision tree provides sufficient accuracy compared to ensemble methods. Ensemble methods still improved model performance, as to be expected, but not dramatically. Ensemble methods may not reduce model variance as much due to the large number of samples, which inherently force the decision tree to consider sample variance.

While not considered in the project, quantifying the methods' tradeoff between improved accuracy and model complexity/runtime would prove valuable for picking the overall best model.
