# Used Car Price Analysis

## Overview
In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. The goal is to understand what factors make a car more or less expensive. As a result of this analysis, clear recommendations will be provided to a client -- a used car dealership -- on what consumers value in a used car.

## CRISP-DM Framework
To frame the task, we use the CRISP-DM process, a standard framework in the industry for data projects. This process helps systematically work through a data problem.

The current CRISP-DM Process Model for Data Mining (see Figure 1) was followed.

</br>
</br>
<p align="center">
<img src="images/Figure1_CRISP_DM_Model.jpeg" width="300px" height="300px">
<h4 align="center"> Figure 1</h4>
</p>

### Business Understanding
From a business perspective, the task is to identify key drivers for used car prices. The goal is to provide actionable insights to a used car dealership, helping them understand what features and attributes are most valued by consumers, allowing them to optimize their inventory and pricing strategies.

### Data Problem Definition
To achieve this, an exploratory data analysis (EDA) will be performed on the provided dataset of 426,000 used cars. Statistical and machine learning techniques will be used to identify key features that correlate with car prices. By reframing the business task into these technical steps, meaningful insights can be derived from the data.

## Findings
For the training, 4 different models were used to find the most optimal one:
1. Simple Linear Regression
2. Simple Linear Regression with Polynomial
3. Ridge with Polynomial
4. Lasso with SequentialFeatureSelector and Polynomial

Mean Squared Error (MSE) and R-squared (R2) were used as metrics to penalize large errors and reflect the true accuracy of the models. Both logarithmic and non-logarithmic target variables were considered, and the following results were obtained:

- 'Simple Linear Regression with Polynomial' and 'Ridge with Polynomial' performed the best.
- 'Simple Linear Regression' followed.
- 'Lasso' ranked last.

Notably, utilizing a non-logarithmic target variable resulted in significantly lower error rates.

### Key Feature Analysis
- Factors such as the vehicle’s year, model, odometer reading, transmission type, and cylinder count greatly impact the price prediction.
- Attributes like color, size, and condition play a less critical role in price determination.
- The coefficients of the 'Ridge with Polynomial' model indicated that year and model, as well as combinations like year-odometer and year-cylinders, have substantial influence on price forecasting.

## Deployment
Based on the analysis, several key factors that influence the selling price of used cars were identified. The following recommendations are made:

### Recommendations for Sellers:
- Highlight factors that positively impact selling price, such as larger engine sizes, diesel fuel, automatic transmission, and first ownership, in listings to attract buyers willing to pay a premium.

### Recommendations for Buyers:
- Consider the age of the vehicle when evaluating its price. Older cars tend to have lower prices, but other factors like condition and maintenance history are important.

### Recommendations for Financial Institutions:
- Consider these factors when assessing risk and collateral valuation for used car purchases to make more accurate assessments and informed lending decisions.

### Key Insights:
- The year of manufacture and the model of the vehicle are very influential in predicting the price.
- The odometer reading is inversely related to the price; the more distance traveled, the lower the value of the vehicle (except for classic cars).
- Contrary to what might be expected, the color, condition, and size of the vehicle do not significantly influence the price prediction.
- Some states have higher prices, likely due to factors such as taxes, salaries, and brand preferences.

This analysis provides a comprehensive understanding of the factors affecting used car prices and offers actionable insights for sellers, buyers, and financial institutions.
