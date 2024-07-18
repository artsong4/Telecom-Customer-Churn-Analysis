# Telecom Customer Churn Analysis

This repository contains the final project from the IST 718 Big Data Analytics course. The project leverages data science methodologies to analyze and predict customer churn in the telecom industry. By identifying key factors driving churn and developing predictive models, the study provides actionable insights and strategies to enhance customer retention and loyalty for telecom companies.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Skills Demonstrated](#skills-demonstrated)
4. [Dataset](#dataset)
5. [Analysis](#analysis)
    - [Data Exploration and Preprocessing](#data-exploration-and-preprocessing)
    - [Modeling](#modeling)
    - [Results](#results)
6. [Repository Structure](#repository-structure)
7. [How to Run the Code](#how-to-run-the-code)
8. [Contributors](#contributors)
9. [License](#license)

## Project Overview
In the competitive landscape of the telecommunications industry, retaining customers is as critical as acquiring new ones. Customer churn—the phenomenon where customers switch from one service provider to another—poses a significant challenge and incurs considerable costs. This project aims to leverage data science methodologies to analyze customer data, understand the factors driving churn, and develop predictive models to forecast potential churn, enabling telecom companies to implement targeted retention strategies.

## Objectives
- Analyze customer data to identify key predictors of churn.
- Develop and train machine learning models to predict customer churn.
- Propose strategies for customer retention based on model insights.

## Skills Demonstrated
- Data Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Machine Learning: Logistic Regression, Random Forest, Support Vector Machine
- Data Visualization
- Statistical Analysis

## Dataset
The dataset is sourced from Kaggle and contains details about customer demographics, location, tenure, subscription services, and their status for the quarter. The primary dataset consists of 7043 rows and 38 columns, representing individual customers from a telecommunications company in California during Q2 2022.

### Data Files
- `data/raw/telecom_customer_churn.csv`: Main dataset containing customer details and their churn status.
- `data/raw/telecom_data_dictionary.csv`: Describes each column in the main dataset.
- `data/raw/telecom_zipcode_population.csv`: Provides population data for each zip code.
- `data/processed/cleaned_customer_df.csv`: Processed dataset used for analysis after data cleaning and preprocessing.

### Data Cleaning
The data was cleaned following these steps:
- Removed the Customer ID column as it did not hold valuable information.
- Converted the Zip Code columns from integer to string, ensuring leading zeros were included.
- Merged population data with the main dataset based on zip code.

### Handling Missing Values
- Set missing values in `Avg Monthly Long Distance Charges` to zero.
- Set missing values in `Multiple Lines` to 'No'.
- Set missing values in `Internet Type` to 'None'.
- Set missing values in `Avg Monthly GB Download` to zero.
- Set missing values in various service columns (`Online Security`, `Online Backup`, `Device Protection Plan`, `Premium Tech Support`, `Streaming TV`, `Streaming Movies`, `Streaming Music`, `Unlimited Data`) to 'No'.

## Analysis
### Data Exploration and Preprocessing
The EDA involved analyzing the relationship between various customer attributes and their churn status. This included handling missing values, feature engineering, and visualizing key relationships.

### Modeling
Three models were used to predict customer churn: Logistic Regression, Random Forest Classification, and Support Vector Machine. Each model was evaluated on its accuracy and ability to predict churn.

### Results
- **Logistic Regression**: Best accuracy with unbalanced data: 83.7%
- **Random Forest Classification**: Best accuracy with unbalanced data: 84.6%
- **Support Vector Machine**: Best accuracy with unbalanced data: 84.6%

## Repository Structure
```plaintext
Telecom-Customer-Churn-Analysis/
├── data/
│   ├── raw/
│   │   ├── telecom_customer_churn.csv
│   │   ├── telecom_data_dictionary.csv
│   │   └── telecom_zipcode_population.csv
│   └── processed/
│       └── cleaned_customer_df.csv
├── EDA.ipynb
├── Modeling.ipynb
├── Telecom_Customer_Churn_Analysis_Report.doc
├── README.md
├── LICENSE
