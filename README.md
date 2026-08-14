# Customer Conversion Analysis

This project analyses customer conversion across two marketing contexts using two machine learning algorithms: Logistic Regression and Decision Tree.

## Business Context

The analysis was developed in relation to a Customer and Marketing Data & AI Strategy Consultant role. The aim is to examine how customer and behavioural data can support conversion prediction and data-driven marketing decisions.

## Datasets

### 1. Bank Marketing
Source: UCI Machine Learning Repository  
https://archive.ics.uci.edu/dataset/222/bank+marketing

The `bank-additional-full.csv` dataset contains 41,188 observations and information about direct marketing campaigns conducted by a Portuguese banking institution.

### 2. Online Shoppers Purchasing Intention
Source: UCI Machine Learning Repository  
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

The dataset contains 12,330 online shopping sessions and behavioural variables used to examine whether a session resulted in a purchase.

## Methods

The analysis includes:

- data inspection
- duplicate and missing-value checks
- categorical encoding
- numerical standardisation
- stratified train-test splitting
- Logistic Regression
- Decision Tree
- five-fold cross-validation for Decision Tree tuning
- evaluation using precision, recall, F1 score, ROC-AUC and PR-AUC
- feature interpretation

The Bank Marketing `duration` variable was excluded from the main predictive model because it is only known after a marketing call has occurred and would therefore not be available for pre-contact customer targeting.

## Main Results

| Dataset | Model | Precision | Recall | F1 | ROC-AUC | PR-AUC |
|---|---|---:|---:|---:|---:|---:|
| Bank Marketing | Logistic Regression | 0.359 | 0.645 | 0.461 | 0.800 | 0.446 |
| Bank Marketing | Decision Tree | 0.391 | 0.628 | 0.482 | 0.789 | 0.430 |
| Online Shoppers | Logistic Regression | 0.505 | 0.796 | 0.618 | 0.910 | 0.663 |
| Online Shoppers | Decision Tree | 0.490 | 0.864 | 0.625 | 0.927 | 0.687 |

The results suggest that the two datasets provide complementary insights. Bank Marketing conversion is associated more strongly with economic and campaign-related information, while online conversion is more strongly associated with browsing behaviour.

## Reproducibility

The datasets are not stored in this repository. Download the original datasets from the official UCI links listed above.

The analysis uses:

- `bank-additional-full.csv` from the Bank Marketing archive
- `online_shoppers_intention.csv` from the Online Shoppers Purchasing Intention dataset

Place both files in the same directory as the notebook and run the notebook from top to bottom.
