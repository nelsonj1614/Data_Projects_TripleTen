# Taxi Orders Prediction

**Project:** Develop a machine learning model that accurately predicts the number of airport taxi orders each hour.

<div align="center">
    <img alt="taxi" src="">
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

## Solution Strategy

**Step 1: Data Description and Cleaning**
 In this first section the data is collected and studied. The missing values are estimated or removed. Finally, a initial data description is carried out to get a feel for the data. Therefore some calculations of descriptive statistics are made to get an understanding of the center, spread and frequency of data.

**Step 2: Data Preparation**
Before training, the data must be scaled and split into train, validation and test sets.

**Step 3: Machine Learning Modeling**
The data for each region is fit to a regression model and trained. The RMSE scores of each model are calculated.

**Step 4: Preparation for Profit Calculation**
The minimum total volume of oil and average well capacities are determined. A function is defined to calculate profit.

**Step 5: Risk and Profit Calculation**
Profit is calculated for each region. Bootstrapping used to determine a more realistic estimate for each region with a 95% confidence interval. The region with the greatest mean profit and lowest % risk is selected.

## Machine Learning Applied

#### Linear Regression - Region 0

|  RMSE  | Avg Vol Pred | Avg Vol Actual |
|:------:|:------------:|:--------------:|
| 37.579 |    92.592    |     92.078     |

<div align="center">
    <img alt="oil" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/8f6347a0326b807ccc319554d8ce4b5b30b114dd/03_Oil_Well_Site_Selection_Project/Photos/img1.png">
</div>


#### Linear Regression - Region 1

|  RMSE  | Avg Vol Pred | Avg Vol Actual |
|:------:|:------------:|:--------------:|
| 00.893 |    68.728    |     68.723     |

<div align="center">
    <img alt="oil" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/8f6347a0326b807ccc319554d8ce4b5b30b114dd/03_Oil_Well_Site_Selection_Project/Photos/img2.png">
</div>


#### Linear Regression - Region 2

|  RMSE  | Avg Vol Pred | Avg Vol Actual |
|:------:|:------------:|:--------------:|
| 40.029 |    94.965    |     94.884     |

<div align="center">
    <img alt="oil" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/8f6347a0326b807ccc319554d8ce4b5b30b114dd/03_Oil_Well_Site_Selection_Project/Photos/img3.png">
</div>


## Profit and Risk

- To assess risk and get a more realistic estimate for the actual amount of revenue the company can gain, the bootstrapping technique is used.
- Since the company will test 500 wells before selecting 200 from those 500, I have set the sample size to 500. Sampling is also with replacement, so the same well can be selected more than once.
- 1000 samples are made and the profit is calculated. Profit of the sample is added to a list of values. From here the upper and lower values of a 95% confidence interval are returned as well as the mean and risk of loss.

#### Region 1:

- **Projected average volume of top 200 wells:** 155.511
- **Projected profit from top 200 wells:** 33,208,260.431
- **Realistic Estimate after Bootstrapping:**
1. With 95% confidence, we can say that the mean profit will fall somewhere between 12,311,636 and 129,483.
2. Mean: 6,007,352
3. Risk of loss: 2.00%

#### Region 2:

- **Projected average volume of top 200 wells:** 138.730
- **Projected profit from top 200 wells:** 24,150,866.966
- **Realistic Estimate after Bootstrapping:**
1. With 95% confidence, we can say that the mean profit will fall somewhere between 11,976,416 and 1,579,885.
2. Mean: 6,652,411
3. Risk of loss: 0.30%

#### Region 3:

- **Projected average volume of top 200 wells:** 148.019
- **Projected profit from top 200 wells:** 27,103,499.635
- **Realistic Estimate after Bootstrapping:**
1. With 95% confidence, we can say that the mean profit will fall somewhere between 12,306,445 and -122,185.
2. Mean: 6,155,597
3. Risk of loss: 3.00%
