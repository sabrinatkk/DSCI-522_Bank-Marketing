# Bank Marketing

<img src="https://www.freeiconspng.com/uploads/estrat-gia-foco-e-assertividade-para-o-marketing--15.png" class="center" width="400" height="200">

### Team members:

* Brenden Everitt (github id: everittb)

* Sabrina Kakei Tse (github id: sabrinatkk)

--------------------------------------------------
## Overview:  

### 1. Motivation  
Marketing a new product directly to clients is often an expensive task undertaking by many companies. However, what if there was a smarter and more efficient way to direct your resources so you only contact clients that you believed were willing to sign-up or purchase a new product? This was the case with a Portuguese Bank that had a new fixed term deposit that they wanted to market to their existing clients. Our goal was to develop a model that given a set of customer features could predict whether or not that customer would sign-up for this new term deposit.

### 2. Dataset:

#### Inputs = 15 attributes of existing bank customers and datatype  
| Data Type   | Variables   |
|:-----------:|:-----------:|
| numeric     | age, balance, day, campaign, previous |
| categorical | job, marital, education, default, housing, loan, contact, month, poutcome, pdays|

source:https://archive.ics.uci.edu/ml/datasets/Bank+Marketing

[Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, Elsevier, 62:22-31, June 2014

### 3. Question
**Type:** Predictive

_Will an existing bank customer sign up to a new term deposit through a direct marketing campaign?_

### 4. Background

![](./results/imgs/data_loaded.jpg)  

The dataset was generated by a phone marketing campaign run by a Portuguese bank. The campaign aimed to encourage the bank's existing customers to sign up for a new term deposit. The dataset contains ~45,000 examples with both quantitative and qualitative data on 20 features for each customer. The dataset also includes the final result of previous campaign that indicates successful sign-ups.  


### 5. Plan

We are going to build a Decision Tree Classifier to identify which characteristics of the clientele will lead to subscription to the new bank product.

1. **Importing and cleaning data**- For variables, we will only consider 15 customer attributes. We excluded `duration` because when predicting whether or not a customer will sign up if they are contacted, it is impossible to know the duration of the call beforehand . In addition, we will also exclude the social and economic attributes: `emp.var.rate, cons.price.idx, cons.conf.idx, euribor3m, and nr.employed` because they are macro-economic factors that are not directly related to the customers that we want to study.

2. **Exploratory Data Analysis** - For categorical variables, seaborn catplot will be used to plot the variable of interest against the target variable, which is `sign-up `. For continuous variables, seaborn boxplot will be used instead. We will include some of the most interesting graphs in the final report.

3. **Hyperparameter for Decision Tree** - we will use k-fold cross-validation to pick the maximum depth of the tree.

### 6. Presentation:

- [x] Decision Tree Model to predict whether or not an existing customer will sign up for a new bank product through the new marketing campaign. We will provide:

  - The full tree in pdf as a reference
  - The top two layers of the tree
  - Test accuracy for the final model  

- [x] Table to summarize the features selected by the classifier

  - This table ranks all of the customer features used in the model by Gini importance

### 7. Package requirements and scripts

NOTE: The scripts are to be run at the main directory

**Dependencies**

| Language   | Packages  |
|:-----------:|:-----------:|
| Python(3.6.5 :: Anaconda, Inc.) | `panada(0.23.0)`, `argparse`, `numpy(1.14.3)`, `matplotlib(2.2.2)`, `graphviz(0.10.1)`, `sklearn(0.19.1)`, `seaborn(0.9.0)` |
| R(3.5.0)   | `knitr(1.20)`, `tidyverse(0.2.5)` |

**Data Analysis Pipeline - Make**

Please use this command line to:

To create report

``` make all ```

To clean intermediate information

``` make clean ```


### 8. Final Report

Please click [here](https://github.com/UBC-MDS/DSCI-522_Bank-Marketing/blob/master/documents/Bank-Marketing-Findings.md)
