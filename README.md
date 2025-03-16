# Customer Churn Analysis

## Table of Contents
[Dataset Overview](#Dataset-Overview)
a. Removed Unnecessary Columns

b. Handled Categorical Data

c. Checked for Missing Values

d. Analyzed Numerical Columns

[Data Cleaning Steps](#Data-Cleaning-Steps)

[Data Analysis Insights](#Data-Analysis-Insights)

[Churn Prediction Analysis](#Churn-Prediction-Analysis)

[Recommendations to Address Customer Churn](#Recommendations-to-Address-Customer-Churn)


1. ## Dataset Overview

 This dataset contains 7043 customer records related to telecom services, providing insights into customer demographics, service subscriptions, account information, and churn behavior. The key columns include:

**Customer Information**: customerID, gender, SeniorCitizen, Partner, Dependents

**Service Details**: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies

**Account Information**: Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, tenure

**Support Tickets**: numAdminTickets, numTechTickets

Target Variable: Churn (Yes/No)

## The dataset helps in analyzing customer churn patterns and identifying factors contributing to customer retention.

2. ## Data Cleaning Steps

a. Removed Unnecessary Columns

Dropped Unnamed: 0 and new gender columns as they contained only NaN values.

b. Handled Categorical Data

Replaced "No internet service" and "No phone service" values in multiple columns with "No" to maintain consistency.

c. Checked for Missing Values

No missing values were found in the dataset apart from the already dropped columns.

d. Analyzed Numerical Columns

Found that TotalCharges had some 0 values. Upon further inspection, all customers with TotalCharges = 0 had tenure = 0, meaning they were new customers. No correction was needed.

3. ## Data Analysis Insights

a. Customer Tenure

Customers have a tenure ranging from 0 to 72 months.

A significant number of customers are in the early months (0-12 months), which might indicate higher churn risk.

b. Monthly and Total Charges

Monthly charges range from $18.25 to $118.75.

TotalCharges varies from $0 to $8684.80.

c. Churn Rate

Churn is the target variable, which consists of "Yes" and "No" values.

Further analysis will determine key factors affecting churn.

4. ## Churn Prediction Analysis

a. **Key Factors Influencing Churn**

Based on initial data exploration, the following factors are strong predictors of customer churn:

Tenure – Customers with lower tenure (0-12 months) are more likely to churn.

Monthly Charges – Higher monthly charges may lead to increased churn.

Contract Type – Customers on month-to-month contracts tend to churn more than those with longer-term contracts.

Internet Service Type – Customers using Fiber optic may have a higher churn rate compared to DSL or No Internet service.

Tech Support & Security Services – Customers without Tech Support or Online Security have a higher churn probability.

Payment Method – Customers using electronic check payments show a higher likelihood of churn compared to other payment methods.

b. **Predictive Modeling Approach**

To validate these churn drivers, the following techniques were used in Excel:

Correlation Analysis – Analyzed the correlation between churn and key factors using Excel’s correlation matrix.

Pivot Tables & Conditional Formatting – Created pivot tables to visualize churn trends and applied conditional formatting to highlight key patterns.

Logistic Regression (Excel Solver) – Used Excel’s Solver to perform logistic regression and assess the impact of different features on churn probability.

Charts & Dashboards – Developed visual representations of churn drivers using Excel charts to track trends and identify high-risk customers.

5. ## Recommendations to Address Customer Churn

a. Improve Customer Retention Strategies

Implement personalized retention campaigns targeting customers with low tenure and high churn probability.

Offer loyalty rewards or discounts to long-term customers.

b. Enhance Customer Support

Strengthen technical support and customer service to address complaints efficiently.

Provide proactive assistance to customers facing service disruptions.

c. Adjust Pricing and Contract Options

Introduce flexible pricing models and promotional discounts to retain customers.

Encourage customers to opt for long-term contracts by offering incentives.

d. Optimize Service Offerings

Improve internet service reliability and speed to reduce churn among internet users.

Enhance bundled service offerings to provide more value to customers.

e. Leverage Data Analytics

Use Excel tools to monitor churn patterns and detect early warning signs.

Predict high-risk churn customers and intervene with retention strategies proactively.

