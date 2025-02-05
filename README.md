# Used Car Price Prediction Model

## Project Overview
This repository contains the a Jupyter notebook that explores a used car dataset and creates regression models for predicting used car prices based on various features such as year, mileage, manufacturer, and type. The goal of this project is to provide used car dealers with insights that can help them optimize their inventory and pricing strategies.

## Data

### Overview
The data for this project consists of a dataset of used cars, which includes various features such as age, mileage, manufacturer, and other car-specific characteristics. This dataset was used to develop models that predict the prices of used cars based on these features.

### Key Variables
- **Age**: The current year minus the year the vehicle was manufactured, transformed using the natural logarithm to normalize its distribution.
- **Odometer**: The mileage of the car in miles, also transformed using the natural logarithm to normalize its distribution.
- **Manufacturer**: The brand of the car.
- **Fuel**: The type of fuel the car uses.
- **Transmission**: The type of transmission in the car.
- **Drive**: The type of drivetrain in the car.
- **Type**: The body type of the car.
- **Title Status**: The legal status of the car (e.g., clean, salvage).

### Preprocessing
Data preprocessing involved cleaning missing values, encoding categorical variables using one-hot encoding, and transforming skewed numeric variables to improve model accuracy and performance.

### Visualization of the Data
Below is a plot showing the distribution of car prices by manufacturer after data clipping, which helps in understanding how car prices vary across different manufacturers.

![Price Distribution by Manufacturer](/plots/manufacturer_after_clip.png)

This visualization provides insights into which manufacturers tend to have higher price points, potentially influencing inventory decisions for used car dealers.

## Key Findings

### Predictive Power of Features
The analysis revealed that certain features are particularly influential in predicting used car prices:
- **Year**: Older cars tend to have lower prices, with the vehicle age being the most significant predictor in the models.
- **Mileage**: Higher mileage on cars generally leads to lower prices, indicating wear and usage impact.
- **Manufacturer**: The company that made the vehicle influenced its price, with premium brands garnering higher prices.
- **Vehicle Type**: The type of vehicle (e.g. sedan, truck, van, etc.) had an importance roughly on par with the manufacturer and mileage.
- **Cylinders**: The number of cylinders in a car influences its price, reflecting engine size and performance capabilities.

### Model Performance
- The **Ridge Regression** model performed the best among the ones tested, with an optimal balance of bias and variance, suggesting it as a suitable model for deployment in predictive tasks.
- **Linear Regression** also provided valuable insights but was slightly less effective in terms of predictive accuracy and handling multicollinearity.
- **Lasso Regression** performed the worst out of the three and was the slowest to train.

### Practical Applications
- These insights can assist used car dealers in setting more competitive pricing and selecting cars that are more likely to retain value over time.
- Understanding these key drivers helps in marketing strategies, focusing on attributes that contribute positively to a car’s valuation.

### Future Recommendations
- Further data collection filling in missing data in columns such as 'type' and 'size' and/or in some manner incorporating the 'model' column could potentially improve model accuracy.
- Regular model updates and retraining with new data are recommended to adapt to changing market conditions and trends.


## View Notebook
You can view the Jupyter notebook [directly on GitHub](prompt_II.ipynb) or via this [nbviewer link](https://nbviewer.org/github/monomial/ucbai-pa-ii/blob/main/prompt_II.ipynb).

## Getting Started

### Prerequisites
Before running this project, you need to have Python installed on your system along with the following libraries:
- pandas
- numpy
- scikit-learn
- matplotlib

### Installation
Clone this repository to your local machine:
```bash
git clone https://github.com/monomial/ucbai-pa-ii.git
cd ucbai-pa-ii
```
