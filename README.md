# Customer Churn Analysis - Fitly

## Project Overview
This project focuses on analyzing customer churn for a fitness application ("Fitly"). The primary objective is to identify the key drivers behind user cancellations and provide actionable business recommendations to improve customer retention. 

This analysis was developed as part of a Data Analyst Professional practical assessment.

## Business Problem
The leadership team is concerned about the rate at which users are canceling their subscriptions. They need to understand:
* What is the current churn rate?
* Are there specific user segments or behaviors associated with higher churn?
* What operational bottlenecks (e.g., customer support) contribute to users leaving?

## Data Sources
The analysis is based on three internal datasets:
1. **Account Information:** Customer demographics, subscription plan types, list prices, and churn status.
2. **Customer Support:** Log of support tickets, including channels, topics, and resolution times.
3. **User Activity:** Event-level data tracking user engagement (e.g., watching videos, tracking workouts).

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

## Methodology
The project follows a standard data analysis pipeline:

1. **Data Wrangling & Cleaning:**
   * Handled missing values (e.g., assuming null churn statuses represented active users).
   * Standardized data formats (converting string timestamps to datetime objects, standardizing customer IDs across tables).
   * Cleaned anomalous values (negative prices, missing categorical labels).
2. **Data Aggregation & Merging:**
   * Aggregated event-level activity data and support tickets to the customer level.
   * Performed Left Joins to create a single, comprehensive dataset for analysis.
3. **Exploratory Data Analysis (EDA):**
   * Built visualizations to compare retention across different subscription plans.
   * Analyzed the correlation between app engagement metrics and churn probability.
   * Evaluated customer support performance metrics between active and churned users.

## Key Findings
* **Overall Churn:** The platform currently has a churn rate of 28.5%.
* **Customer Support Impact:** There is a massive disparity in support quality. Retained users had an average ticket resolution time of ~6.0 hours, while churned users waited an average of ~17.8 hours.
* **Engagement Drop-off:** Churned users exhibited significantly fewer total in-app activities. Lack of product usage is a strong leading indicator of churn.
* **Plan Vulnerability:** The 'Free' and 'Basic' plans experience the highest churn rates (over 40%), indicating a potential issue with perceived value or onboarding in lower tiers.

## Business Recommendations
Based on the data, I recommend the following actions to reduce churn:
1. **Implement Support SLAs:** Customer Support must establish a Service Level Agreement (SLA) to resolve all technical and account issues in under 8 hours. Waiting 17+ hours is a primary driver of cancellation.
2. **Launch Re-engagement Campaigns:** Marketing and Product teams should set up automated triggers for users showing 0 or 1 activities. Push notifications or emails should be used to bring them back to the app before they cancel.
3. **Optimize Lower-Tier Onboarding:** Product Management should investigate the onboarding flow for 'Free' and 'Basic' users. Offering a time-limited "Pro" trial could demonstrate the app's full value and encourage upgrades rather than churn.

## Key Metrics to Monitor
To track the success of retention initiatives, the business should continuously monitor:
* **Customer Churn Rate** (Baseline: 28.5%)
* **Average Support Resolution Time** (Baseline target: < 6.0 hours)

## How to Run This Project
1. Clone the repository.
2. Ensure you have Python and the required libraries installed (`pip install pandas numpy matplotlib seaborn`).
3. Open the `notebook.ipynb` file in Jupyter or any compatible IDE to view the code, data processing steps, and visualizations.
