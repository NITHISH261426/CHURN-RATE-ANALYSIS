# CHURN-RATE-ANALYSIS
An end-to-end customer churn analysis project using Power BI. It leverages DAX for complex KPIs and Power Query for data transformation to build a dynamic dashboard. The goal is to translate data into actionable business insights.

## Project Overview

Customer churn is a critical issue for any subscription-based business. This project performs an in-depth Exploratory Data Analysis (EDA) on a telecom customer dataset to understand the key drivers of churn. The goal is to move beyond simple observations to uncover actionable, data-driven insights that can help a business formulate effective retention strategies.

The final output is a dynamic and interactive Power BI dashboard that not only visualizes the data but also tells a clear story about why customers leave and what can be done about it.

## 🛠️ Technical Stack

*   **Power BI Desktop:** Used for data modeling, DAX calculations, and all visualizations.
*   **DAX (Data Analysis Expressions):** Used to create complex measures for dynamic calculations (e.g., Churn Rate,  customer counts).
*   **Power Query :** Used for data cleaning, transformation, and creating conditional columns (e.g., Tenure Groups).

## 📂 Data Source

The dataset used for this analysis is the "Customer Churn" dataset, widely available on platforms like Kaggle. It contains demographic, account, and service information for over 7,000 customers.
- <a href="https://github.com/NITHISH261426/CHURN-RATE-ANALYSIS/blob/main/02%20Customer%20Churn-Dataset.xlsx">Dataset</a>


### Data Dictionary

The dataset contains `7043` customer records and `23` features.

| Column Name | Data Type | Description | Notes / Example Values |
| :--- | :--- | :--- | :--- |
| `customerID` | `object` | A unique identifier for each customer. | e.g., `7590-VHVEG` |
| `gender` | `object` | The customer's gender. | `Male`, `Female` |
| `SeniorCitizen` | `int64` | Indicates if the customer is a senior citizen (1) or not (0). | `0`, `1` |
| `Partner` | `object` | Indicates if the customer has a partner. | `Yes`, `No` |
| `Dependents` | `object` | Indicates if the customer has dependents. | `Yes`, `No` |
| `tenure` | `int64` | The total number of months the customer has been with the company. | `1`, `24`, `72` |
| `PhoneService` | `object` | Indicates if the customer has a phone service. | `Yes`, `No` |
| `MultipleLines` | `object` | Indicates if the customer has multiple phone lines. | `Yes`, `No`, `No phone service` |
| `InternetService`| `object` | The type of internet service the customer has. | `DSL`, `Fiber optic`, `No` |
| `OnlineSecurity` | `object` | Indicates if the customer has the online security service. | `Yes`, `No`, `No internet service` |
| `OnlineBackup` | `object` | Indicates if the customer has the online backup service. | `Yes`, `No`, `No internet service` |
| `DeviceProtection`| `object` | Indicates if the customer has the device protection service. | `Yes`, `No`, `No internet service` |
| `TechSupport` | `object` | Indicates if the customer has the tech support service. | `Yes`, `No`, `No internet service` |
| `StreamingTV` | `object` | Indicates if the customer has a TV streaming service. | `Yes`, `No`, `No internet service` |
| `StreamingMovies`| `object` | Indicates if the customer has a movie streaming service. | `Yes`, `No`, `No internet service` |
| `Contract` | `object` | The customer's contract term. | `Month-to-month`, `One year`, `Two year`|
| `PaperlessBilling`| `object` | Indicates if the customer uses paperless billing. | `Yes`, `No` |
| `PaymentMethod` | `object` | The customer's payment method. | `Electronic check`, `Mailed check`, etc. |
| `MonthlyCharges` | `float64`| The amount charged to the customer monthly. | e.g., `29.85` |
| `TotalCharges` | `object` | The total amount charged to the customer over their tenure. | **Note:** This column requires conversion to a numeric type. |
| `numAdminTickets` | `int64` | The number of administrative support tickets filed by the customer. | e.g., `0`, `1`, `5` |
| `numTechTickets` | `int64` | The number of technical support tickets filed by the customer. | e.g., `0`, `2`, `7` |
| `Churn` | `object` | **(Target Variable)** Indicates if the customer churned. | `Yes`, `No` |



## Key Findings & Actionable Insights

My analysis revealed several critical insights that directly inform retention strategy:

*   **The Fiber Optic Paradox:** While being a premium service, customers with **Fiber Optic** internet have an alarmingly high churn rate of **42%**, more than double that of DSL users (19%). This suggests a mismatch between price, performance expectations, and service reliability.
*   **Payment Friction is a Major Driver:** Customers using manual payment methods like **Electronic Check** churn at a rate of **45%**. In contrast, those on **Automatic Payments** have a much lower churn rate of just 15%.
*   **The "Leaky Bucket" of New Customers:** The **Line & Stacked Column Chart** clearly shows that the highest churn rates occur within the first 12 months. This is especially risky as this new customer segment also contributes a significant portion of the total Monthly Recurring Revenue (MRR).
*   **Support Tickets as a Leading Indicator:** A customer's likelihood to churn increases dramatically with the number of tech support tickets filed. Customers with 3 or more tickets have a churn rate exceeding **65%**, making support interaction a powerful predictive signal.


## 📊 Power BI Report

To present findings in an accessible and interactive format, a dashboard was created using Microsoft Power BI. This dashboard allows stakeholders to dynamically filter the data and explore sales trends on their own.

- <a href="https://github.com/NITHISH261426/CHURN-RATE-ANALYSIS/blob/main/CHURN%20ANALYSIS.pbix">PowerBIReport</a>
