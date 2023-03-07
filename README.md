# Credit Risk Analysis

## Overview

In this analysis we look at a high dimensional data set of loan recipients and repayment data; using this data, we build a variety of classification models using different resampling methods. The hope is to find a model which can strongly predict the risk categories -- high risk or low risk -- of potential customers to allow for more effective decision making in approving or denying loan requests.

## Results

Below we present the balanced accuracy score and classification report for each of six different classifications models built using different resampling/decision tree methods. The classification reports are presented as images for clarity; for our comparisons of the models, we focus on the precision (pre) and recall (rec) in each table. The balanced accuracy score computations can be found in the notebooks found in this archive.

- Naive Random Oversampling:
  - balanced accuracy score: 0.668
  - classification report. 
  
  ![](https://raw.githubusercontent.com/SecretDoves3000/Credit_Risk_Analysis/main/images/ROSS.png)
