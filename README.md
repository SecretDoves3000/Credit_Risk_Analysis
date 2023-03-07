# Credit Risk Analysis

## Overview

In this analysis we look at a high dimensional data set of loan recipients and repayment data; using this data, we build a variety of classification models using different resampling methods. The hope is to find a model which can strongly predict the risk categories -- high risk or low risk -- of potential customers to allow for more effective decision making in approving or denying loan requests.

## Results

Below we present the balanced accuracy score and classification report for each of six different classifications models built using different resampling/decision tree methods. The classification reports are presented as images for clarity; for our comparisons of the models, we focus on the precision (pre) and recall (rec) in each table. The balanced accuracy score computations can be found in the notebooks found in this archive.

- Naive Random Oversampling:
  - balanced accuracy score: 0.651
  - classification report: 
  
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/ROSS.png)
 
- SMOTE Oversampling:
  - balanced accuracy score: 0.685
  - classification report: 
 
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/SMOTESS.png)
  
- Cluster Centroid Undersampling:
  - balanced accuracy score: 0.549
  - classification report: 
  
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/CCSS_s.png)
  
- SMOTEEN combination sampling:
  - balanced accuracy score: 0.657
  - classification report: 
  
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/SMOTENSS.png)
  
- Balanced Random Forest Classifier:
  - balanced accuracy score: 0.668
  - classification report: 
  
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/BRFSS.png)
  
- AdaBoost Classifier:
  - balanced accuracy score: 0.703
  - classification report: 
  
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/EEABSS.png)
  
## Summary
  
In terms of approving loans, for any model we use, of course being as accurate as possible is ideal. However, in terms of acceptable innacuracy, mislabling high-risk loans as low-risk presents a much more significant risk than mislabling low-risk loans as high. In terms of our classification reports, this means we want as high of a recall -- the percentage of correctly predicted positives -- for the high-risk category as possible. Of our models, the SMOTEEN combination sampling has the highest recall for high-risk loans at 71%. It's balanced accuracy is relatively low, however at 0.657 which reflects the fact that the high-risk precision -- the percentage of predicted high-risk loans which were actually high-risk -- is extremely low at 1%. 

Even at 71% recall for high-risk loans, this means our most defensive model would still leave 29% of the actually high-risk loans would be predicted as low-risk. Almost 30% classification of high-risk as low risk is still precipitously high in our opinion. As such, we should gather more data and reconsider our overall approach in using these models. 
