# predict**Sales**

Author: Sheneka Allen


---


# Business problem:
>This model was created to help retailers better understand the properties of products and stores/outlets that impact sales numbers.

# Data:
>This dataset supports sales predictions for food items sold at various stores.

>Original Data Source: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

# Methods:

1.   Explore the data to identify missing values and identify correlations (create a heatmap).
2.   Find and fix any category inconsistencies.
3.   Determine category types for column values (nominal, ordinal) and discern best approach for imputation (i.e., small=0, medium=1, large=2).
4.   Determine value you want to predict or target (y) then define target and features (X) vectors.  In this case, I chose 'Item Outlet Sales' since the focus is on predicting sales based on other features (X) in the dataset.
5.   Perform a random train-test-split (default split of 75/25 is fine).
6.   Create a pre-processing pipeline to transform and normalize ALL dataset values for machine learning.
7.   Fit pre-processor on the TRAINING data (to avoid leaking data to test set).
8.   Confirm dataset is effectively cleaned (i.e., no missing values, data is properly scaled and processed).
9.   Explore at least two regression models to evaluate best which has the most favorable impact on model performance.  Compare metrics R2 and RMSE to justify recommendation.
10.   Create at least two visualizations for this dataset to support analysis.

---




# Insights and Results: 

![salesbystore1](https://user-images.githubusercontent.com/100389581/166484069-0e10e156-b46e-44b6-816f-d83c2c2f9af4.png)

>Supermarket Type 3 is the clear winner in sales($) for all the Outlet Types at 3600.

>Grocery Stores is the clear underperformer in sales for all the Outlet Types at about $400

>Supermarket Types 1 & 2 are closer in sales ($2000 to 2400 range), but still underperform Supermarket Type 3.


![itemsalesbyoutlet1](https://user-images.githubusercontent.com/100389581/166484108-b75bc68f-1aba-4725-a454-92c0ae30965c.png)

It appears that the Top Three item types with the highest averages in sales are:

>Starchy Foods

>Seafood

>Possible tie between Fruits and Vegetables, Snack Foods

---
# Recommendations:
>After reducing the max_depth() parameter from None to 10 and comparing metrics (R2, RMSE), the Random Forest Regressor model performance appears to be the best in this case. Variance is significantly reduced and the bias is higher, which improves the prediction performance on unknown/test data.

>Overall, which model do YOU recommend?  Why?


# For further information:
For any additional questions, please contact: https://www.linkedin.com/in/shenekaallen/
