# Optimizing New York City Taxi Services through Predictive Analytics

## Overview
This project leverages predictive analytics to optimize New York City taxi services by uncovering patterns in fare pricing and operational inefficiencies. By analyzing the TLC Trip Record Data, we aim to address issues such as overcharging and suboptimal pricing systems through rigorous data exploration, feature engineering, model development, hyperparameter tuning, and result evaluation. Our goal is to provide actionable insights that can empower both customers and taxi companies to achieve fairer and more efficient taxi operations.

## Installation
To set up your environment for running the analysis notebook (e.g., `NYC_Taxi_Predictive_Analytics.ipynb`), please ensure you have the following dependencies installed:
1. **Python 3.7+**
2. **Required Libraries:**  
   Create a `requirements.txt` file with the following contents:
   ```
   numpy
   pandas
   scikit-learn
   matplotlib
   seaborn
   xgboost
   lightgbm
   catboost
   ```
3. **Installation Command:**  
   Run the following command to install these packages:
   ```bash
   pip install -r requirements.txt
   ```

## Project Structure

### Part 1: Introduction
- **Business Problem:**  
  NYC's iconic yellow taxis are vital to urban mobility, yet issues like overcharging and inefficient pricing strategies have raised concerns. Our project tackles these challenges by leveraging machine learning to understand and optimize taxi fare calculations.
- **Data Source:**  
  TLC Trip Record Data – Yellow Taxi Trip Records (direct access available through the provided link).

### Part 2: Data Exploration and Cleaning
- **Tasks Performed:**
  - **Missing Data Handling:** Measured the extent of missing values and pruned incomplete records.
  - **Feature Engineering:** Enriched the dataset by extracting time-related features (e.g., trip duration, granular pickup day and hour).
  - **Data Pruning:** Dropped redundant columns (e.g., `'fare_amount'`) to avoid duplication with the target variable.

### Part 3: Models
- **Modeling Approach:**
  - **Evaluation of Multiple Models:** Compared various machine learning models, including Ridge Regression and Random Forest.
  - **Performance Highlights:**
    - **Ridge Regression:** Nearly perfect R-squared and Explained Variance (~0.974) with low MSE (≈12.409) and RMSE (≈3.523).
    - **Random Forest:** Showed robust performance with a low Mean Cross-Validation MSE (17.409), leading to its selection as the final model.
- **Final Model Selection:**  
  Random Forest was chosen for its consistency and overall predictive accuracy across different data partitions.

### Part 4: Hyper Parameter Search
- **Tuning Strategies Employed:**
  - Grid Search
  - Halving Search
  - Random Search
  - Bayesian Search
- **Observations:**
  - Convergence toward optimal hyperparameter values was observed across all strategies.
  - The Bayesian search uniquely explored the parameter space, maintaining outstanding accuracy.
- **Outcome:**  
  The robust hyperparameter tuning ensured that the final model (Random Forest) was well-optimized for predicting taxi fares.

### Part 5: Feature Importance
- **Analysis:**  
  Conducted a detailed feature importance analysis to identify the key variables influencing taxi fare predictions.
- **Insights:**  
  The analysis provided actionable insights into which features (e.g., trip duration, pickup time components) have the most significant impact on fare calculation.

### Part 6: Results
- **Pipeline Construction:**  
  A complete pipeline was built integrating data preprocessing with the Random Forest model.
- **Performance Evaluation:**  
  The final model was evaluated on a test set, showing strong predictive capabilities and reliable performance metrics.

### Part 7: Implications
- **For Customers:**  
  The data-driven approach allows for transparent fare comparisons with benchmark services like Uber and Lyft, ensuring competitive and fair pricing.
- **For Taxi Companies:**  
  Insights suggest that implementing a dynamic, network-connected meter system—capable of adjusting fares in real-time based on traffic, peak hours, and weather—could enhance operational efficiency and revenue optimization.

### Part 8: Reference
- **Data & Methodologies:**  
  - TLC Trip Record Data – Yellow Taxi Trip Records.
  - Techniques for reading parquet format data and extracting time from datetime fields.
  - Model evaluation metrics and hyperparameter tuning methods (Grid, Halving, Random, Bayesian).
  - Tools and libraries for plotting overlapping line plots and resetting data indices.

## Usage
To run this project:
1. **Setup:**  
   Ensure that you have installed all the required libraries using the provided `requirements.txt`.
2. **Notebook Execution:**  
   Open the `NYC_Taxi_Predictive_Analytics.ipynb` notebook in your Jupyter Notebook or Jupyter Lab environment.
3. **Run Cells:**  
   Execute the notebook cells in sequential order to perform data exploration, model training, hyperparameter tuning, and evaluation.

## Collaborators
- Jiacheng Li
- Shizuka Takahashi
- Unice (Yu-Fang) Liao
