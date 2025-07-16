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






## Key Findings & Actionable Insights

My analysis revealed several critical insights that directly inform retention strategy:

*   **The Fiber Optic Paradox:** While being a premium service, customers with **Fiber Optic** internet have an alarmingly high churn rate of **42%**, more than double that of DSL users (19%). This suggests a mismatch between price, performance expectations, and service reliability.
*   **Payment Friction is a Major Driver:** Customers using manual payment methods like **Electronic Check** churn at a rate of **45%**. In contrast, those on **Automatic Payments** have a much lower churn rate of just 15%.
*   **The "Leaky Bucket" of New Customers:** The **Line & Stacked Column Chart** clearly shows that the highest churn rates occur within the first 12 months. This is especially risky as this new customer segment also contributes a significant portion of the total Monthly Recurring Revenue (MRR).
*   **Support Tickets as a Leading Indicator:** A customer's likelihood to churn increases dramatically with the number of tech support tickets filed. Customers with 3 or more tickets have a churn rate exceeding **65%**, making support interaction a powerful predictive signal.
