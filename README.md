# volve-machine-learning

This repository is my exploration on bringing machine learning to Volve oil field open dataset disclosed by Equinor since 2018. For more information about this dataset and how to access the original database, see [here](https://www.equinor.com/en/how-and-why/digitalisation-in-our-dna/volve-field-data-village-download.html).

#### Machine learning projects (current and upcoming):

* [P-sonic (DT) log prediction in well 15/9-F-11B and 15/9-F-1C]()
* S-sonic (DTS) log imputation 
* Unsupervised classification for facies typing

## P-sonic (DT) log prediction in well 15/9-F-11B and 15/9-F-1C

**Background:** Two wells (well 15/9-F-11B and 15/9-F-1C) don't have P-sonic log. 

**Workflow:**

* Well 15/9-F-11A, 15/9-F-11A, and 15/9-F-1B are used as training data.
* The training data are normalized using Yeo-Johnson method of power transformation, and outliers have been removed using One-Class SVM method.
* Regressors in *Scikit-Learn* used are: Linear Regression, Random Forest, Support Vector Machine, Decision Tree, Gradient Boosting, and K-Nearest Neighbors.
* Best performance achieved by Gradient Boosting.
* Hyperparameter tuning showed the best hyperparameter of GB as follows; `n_estimators`=1,000 and `max_depth`=100
* Average R² and RMSE score achieved are .95 and .12 

**Result:**

The predicted results are written in CSV files; well [15/9-F-11B]() and [15/9-F-1]()


