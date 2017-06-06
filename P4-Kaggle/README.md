### Use of R and h2o to model multi-class outcomes for the [Otto Classification Challenge](https://www.kaggle.com/c/otto-group-product-classification-challenge).

[Training set](https://www.kaggle.com/c/otto-group-product-classification-challenge/data): 93 numeric features + categorical outcome variable with 9 levels, ~60,000 observations

**otto.h2o.R** - h2o modeling using 70/30 train/test split. Hyperparameter tuning/grid search is performed on the GLM model at different weights for ridge and lasso penalties, however no strong ridge or lasso normalization was used. Further parameter tuning could be conducted to identify optimal performance parameters for the random forest and gradient boosted models.

- GLM (Multinomial logistic regression)
- Random forest
- Gradient boosting

Package xgboost was also explored in **otto.xgboost.R** and delivered relatively high test accuracy with limited parameter tuning and at reasonable computation speeds. Although the specific model trained in that script was not used, xgboost was ultimately used to achieve highest team submission accuracy.

For project overview and Kaggle submission results, please visit the [blog post](http://blog.nycdatascience.com/student-works/kaggle-otto-classification/).
