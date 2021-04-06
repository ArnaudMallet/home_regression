# home_regression
Based on Kaggle dataset [link](https://www.kaggle.com/c/house-prices-advanced-regression-techniques), I worked on several approach for linear regression.

Juyter notebook: hr_ll_2.ipynb
1. Straightforward from-the-shelf linear regression using [sklearn](https://scikit-learn.org/stable/) library and [XGBoost](https://xgboost.readthedocs.io/en/latest/)
2. Kaggle Score: 0.13357 with fine tuning

Data Preparation approach:
1. In the training set, 
    a. drop the feature where you have more than 30% of missing value 
    b. Select Quant and Qual value. For qual value with Cardinality below 10
    b. Run Spearman and Pearson correlation to select top XX features 
2. Normalize the training set updated / Normalize the testing set
3. Split the training set in X/Y % to create the validation set
4. Merge the training and dataset 
    a. If one-hot encoding - do it here to make sure that you have every possible options
    b. if Mean Grading & Ordering (preferred solution below) no need for one-hot encoding an it is done during Spearman Correlation
5. Get the training, validation or test sets for .fit() and .predict()

Additional library used:
- Numpy
- Pandas
- Seaborn
- Matplotlib
