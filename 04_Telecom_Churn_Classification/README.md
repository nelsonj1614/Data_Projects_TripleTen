# Telecom Churn Predictor
**Project:** Develop a fast and accurate machine learning model that predicts whether a user will cancel their telecom service plan.

<div align="center">
    <img alt="churn" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/8911af67d0e46966c09d92a498119e9239eeed72/04_Telecom_Churn_Classification/Photos/pikaso_texttoimage_sketch-lines-dissatisfied-phone-user-pencil-drawin.jpg">
</div>

<br>

## Business Problem
Interconnect is a telecom operator that provides two basic services:

- Landline communication. The telephone can be connected to several lines simultaneously.
- Internet. The network can be set up via a telephone line (DSL, digital subscriber line) or through a fiber optic cable.

Additionally they provide:

- Internet security: antivirus software (DeviceProtection) and a malicious website blocker (OnlineSecurity).
  
- Support: A dedicated technical support line (TechSupport).
  
- Storage: Cloud file storage and data backup (OnlineBackup).
  
- Streaming: TV streaming (StreamingTV) and a movie directory (StreamingMovies).

The clients can choose either a monthly payment or sign a 1- or 2-year contract. They can use various payment methods and receive an electronic invoice after a transaction.

**Business Problem:** Interconnect would like to be able to forecast their churn of clients. If it's discovered that a user is planning to leave, they will be offered promotional codes and special plan options. Interconnect's marketing team has collected some of their clientele's personal data, including information about their plans and contracts.

## Solution Strategy

**Step 1: Data Description and Cleaning**
 In this first section the data is collected and studied. The missing values are estimated or removed. Finally, a initial data description is carried out to get a feel for the data. Therefore some calculations of descriptive statistics are made to get an understanding of the center, spread and frequency of numerical and categorical data.

**Step 2: Feature Engineering**
Here, new features are engineered from existing features within the data. These features are meant to give insight during the EDA phase of the project and increase the ability of the ml model to learn from the data.

**Step 3: Data Filtering**
Data that is not relevant or useful to analysis and modeling is removed from the dataset.

**Step 4: Exploratory Data Analysis**
Key insights from the data are explored through data visualization. The class imbalance (Churn), univariate distributions (through histograms and bar charts) and relationships between data (scatterplots) are explored.

**Step 5: Data Preparation**
A pipeline is constructed through which the data can be preprocessed before being passed to a model (estimator). This includes scaling (for numeric features) and encoding (for categorical features).

**Step 6: Machine Learning Modeling**
The data is trained on several models by cross evaluation. At this stage no hyperparameters are tuned. The metric scores of each are recorded and the best performing model proceeds to the next stage.

**Step 7: Hyperparameter Tuning**
The best performing model undergoes hyperparameter tuning via GridSearchCV to find the optimal hyperparamters.

## Data Insights

* #### Insight 1: Monthly Charges Distribution

  
  
* #### Insight 2: Payment Method
  
* #### Insight 3: Plan Type

## Machine Learning Applied

#### Dummy Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

#### Decision Tree Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

#### Gradient Boosting Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

#### XG Boost Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

#### Cat Boost Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

#### Light GBM Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

## Machine Learning Performance

#### Light GBM Model

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

| Balanced Accuracy |  ROC - AUC  |      F1     |Training Time|
|:-----------------:|:-----------:|:-----------:|:-----------:|
|   0.0 +/- 0.0   | 0.0 +/- 0.0 | 0.0 +/- 0.0 | 0.0 +/- 0.0 |

## Business Results

## Conclusions

## Next Steps
