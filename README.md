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

### Key Features of the Dashboard:

This project culminates in a comprehensive analysis that isolates the primary drivers of customer churn. The key findings are summarized below, reflecting the features of a potential interactive dashboard built from this analysis.
#### 1. Executive KPI Scorecard
An at-a-glance view of the most critical business metrics, designed for rapid health assessment.
- **Overall Churn Rate**
- **Total Customers**
- **Monthly Recurring Revenue (MRR)**

#### 2. The "Leaky Bucket" - Tenure & Revenue Analysis
A central Line and Stacked Column chart visualizes the relationship between customer tenure, monthly revenue, and churn rate.
> **Key Insight:** The business struggles with early-tenure churn. The highest churn rates occur within the first few months, especially among customers with high-value services like Fiber Optic internet.

#### 3. Dynamic Root Cause Analysis
Interactive slicers and comparative bar charts empower users to perform self-service analytics and isolate the factors with the highest impact on churn.
> **Actionable Finding:** Payment method is a critical churn driver. Customers using **Mailed check** or **Electronic check** churn at over **3 times the rate** of customers on automatic payment plans. This points to a clear opportunity for intervention by promoting auto-pay.

#### 4. Interactive Deep Dives
Users can dynamically filter the entire analysis by:
- **Internet Service:** Compare churn rates between DSL, Fiber Optic, and non-internet customers.
- **Contract Type:** Instantly see the stabilizing effect of one- and two-year contracts.
- **Payment Method:** Quantify the risk associated with different payment options.

  ## Conclusions & Recommendations

> ### Executive Summary
> This analysis reveals that customer churn is not a random event but a predictable outcome driven by specific points of friction in the customer journey. While the company is successful at acquiring customers, it faces a significant **"leaky bucket" problem**, where a large portion of its most valuable new customers leave within their first year. The following conclusions detail the primary drivers of this issue and are paired with actionable recommendations to improve retention and long-term profitability.

---

### Key Conclusions (What We Learned)

*   **Churn is Heavily Concentrated in the Early Customer Lifecycle.**
    The highest churn rates (**often exceeding 40%**) occur within the first 12 months of a customer's tenure. This high-risk segment also contributes a disproportionately large share of the Monthly Recurring Revenue (MRR), creating significant revenue instability.

*   **Manual Payment Processes Create Significant Churn Friction.**
    Customers using manual methods like *Electronic Check* have an extremely high churn rate of **~45%**, while customers on *Automatic Payments* are far more loyal with a churn rate of only **~15%**. The hassle of manual payment is a major factor in the decision to leave.

*   **Premium Products Create High Expectations and Service Failures are Punished Severely.**
    Customers with the premium *Fiber Optic* service churn at **over 40%**, more than double the rate of DSL customers. This is because the high price sets high expectations. When these customers encounter technical issues, their frustration is amplified, leading to rapid churn.

*   **Customer Engagement with Add-On Services is a Strong Indicator of Loyalty.**
    Customers who subscribe to multiple value-add services (like *Device Protection*, *Online Backup*, *Tech Support*) are significantly less likely to churn. These services create a `"stickier"` relationship, increasing the customer's investment in the company's ecosystem.

---

### Strategic Recommendations (What We Should Do)

1.  **Launch a Proactive "First 90-Day" Onboarding Program.**
    *   **Action:** Implement a structured onboarding process, including a welcome call, a 30-day satisfaction check-in, and proactive technical monitoring for new Fiber Optic customers.
    *   **Goal:** Reduce first-year churn by at least 20%, turning unstable new revenue into a stable, long-term asset.

2.  **Incentivize the Shift to Automatic Payments.**
    *   **Action:** Roll out a targeted marketing campaign offering a one-time bill credit (**$5 or $10**) to all customers who switch from a manual payment method to an automatic one.
    *   **Goal:** Directly target a high-churn segment with a low-cost, high-impact solution to immediately improve retention.

3.  **Implement "White-Glove" Support for Premium (Fiber) Customers.**
    *   **Action:** Create a **"two-ticket" rule**: any Fiber Optic customer who logs a second technical support ticket within six months is automatically flagged for a proactive follow-up from a senior retention specialist.
    *   **Goal:** Manage the high expectations of high-value customers, resolve their frustrations before they escalate, and protect a crucial revenue stream.

4.  **Develop and Promote "Value-Add" Service Bundles.**
    *   **Action:** Create and market *"Peace of Mind"* or *"Total Protection"* bundles during sales and onboarding, including services like Online Security, Device Protection, and Tech Support at a discounted rate.
    *   **Goal:** Increase customer "stickiness" from day one, raising the switching cost and building a more integrated and loyal customer base.
