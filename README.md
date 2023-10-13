# Hackathon
Repository for predicting RUL for Turbo Fan Jet Engine

# Running the Notebook
1. Create a sub-folder called input from your working directory and copy the source files train_FD001.txt, test_FD001.txt and RUL_FD001.txt
2. You may need to install the libraries used in the notebook
3. The following libraries have been used in the notebook
   a. os
   b. pandas
   c. matlplotlib
   d. numpy
   e. seaborn
   f. time
   g. contextlib
   h. warnings
   i. sklearn
   j. statsmodels
   k. hyperopt
   j. xgboost
   l. lightgbm
   m. carboost
4. If you want to use other files to train your model such as train_FD002.txt, you should use appropriate test and results file such as test_FD002.txt and RUL_FD002.txt.
   ## Note: training with a different file may need different feature engineering methods and could result in a different model
   
# Data
The Data for this notebook was sourced from Kaggle https://www.kaggle.com/datasets/behrad3d/nasa-cmaps

# Data Preprocessing
1.  The data does not have any nulls
2.  Outliers were not removed   
   
#  Feature Engineering
1.  Features deemed irrelevant were dropped
2.  Standard Scaling was applied to the survived features
3.  Log transform was applied to the target

#  Modelling
1. Several algorithms were compared against unscaled and scaled features
2. CatBoost had the best R2 and RMSE score on test dataset
3. LighGBM was selected as the final best feature due to faster training time and 2nd best R2 and RMSE scores
4. LighGBM was further tuned using Bayesian hyperparameter tuning using Hyperopt

# Results
The final model achieved R2 score of 0.5617, MAE of 19.871 and RMSE of 27.509
