# Oil Well Site Selection

**Project:** Find the best place to drill a new well by creating a machine learning model to predict the capacity of oil reserves in each region.

<div align="center">
    <img alt="oil" src="">
</div>

<br>

## Business Problem
Oily Giant wants to drill a new oil well. Before they do this, they need to know where to drill the new well. There are three regions available for well drilling. This goal of this analysis is to identify the most profitable region to drill a new well.
I begin by training linear regression models on the 3 datasets provided. From this model, I select the oil wells that have the highest predicted reserve volumes. Of these selected wells, I perform calculations to assess which region is most profitable. 

**Data:** Data consists of 3 CSV files. Each file contains wells from a region. In addition to an identifying well ID, each row includes three estimated values (f0,f1,f2) and a 'product' value which is an estimation of the well volume.

**Steps to choose the location:**

- Collect the oil well parameters in the selected region: oil quality and volume of reserves;
- Build a model for predicting the volume of reserves in the new wells;
- Pick the oil wells with the highest estimated values;
- Pick the region with the highest total profit for the selected oil wells.

You have data on oil samples from three regions. Parameters of each oil well in the region are already known. Build a model that will help to pick the region with the highest profit margin. Analyze potential profit and risks using the Bootstrapping technique.

## Solution Strategy

**Step 1: Data Description and Cleaning**
 In this first section the data is collected and studied. The missing values are estimated or removed. Finally, a initial data description is carried out to get a feel for the data. Therefore some calculations of descriptive statistics are made to get an understanding of the center, spread and frequency of data.

**Step 2: Data Preparation**
Before training, the data must be scaled and split into train, validation and test sets.

**Step 3: Machine Learning Modeling**
The data for each region is fit to a regression model and trained. The metric scores of each model are recorded.

**Step 4: Preparation for Profit Calculation**

**Step 5: Risk and Profit Calculation**

## Machine Learning Applied

#### Linear Regression - Region 0

| Accuracy | Precision | Recall |  F1   | Roc-Auc |
|:--------:|:---------:|:------:|:-----:|:-------:|
|   0.731  |  0.000    |  0.000 | 0.000 |   0.500 |

#### Linear Regression - Region 1

| Accuracy | Precision | Recall |  F1   | Roc-Auc |
|:--------:|:---------:|:------:|:-----:|:-------:|
|   0.813  |  0.648    |  0.665 | 0.656 |   0.500 |

#### Linear Regression - Region 2

| Accuracy | Precision | Recall |  F1   | Roc-Auc |
|:--------:|:---------:|:------:|:-----:|:-------:|
|   0.854  |  0.831    |  0.573 | 0.678 |   0.899 |
