# 📈 Predictive Bank Customer Churn Analysis and Effective Retention Strategy Recommendation | Power BI

**Author:** Lê Gia Bảo

**Date:** August 2025

**Tools Used:** Power BI

## 📑 Table of Contents  
1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---

## 📌 Background & Overview  

**📖 What is this project about?**

The main goal of this project is to use historical data to **analyze** customer behavior and build a **predictive** model to identify customers at high risk of **churn** (*attrition*)

The main goal is to give senior managers **clear, data-backed insights** so they can:

* **Understand current business performance** (See how well the company is doing right now).
* **Optimize market expansion strategies** (Figure out the best ways and places to grow the business).
* **Identify strategic products for growth** (Find the products that should be prioritized for maximum success).
* **Support better decision-making to drive revenue** (Use facts to make choices that boost sales).

**👤 Who is this project for?**

✔️ Data Analysis: Build risk prediction models and identify core drivers of customer churn

✔️ Marketing & Retention: Improve retention rates with targeted intervention campaigns, increasing customer value.

✔️ Strategy & Operations: Optimize service channels and resources in high-risk areas.


**❓Business Questions:**

✔️ Which behavioral and product-related factors are the strongest drivers of churn?

✔️ What are the most impactful intervention points for optimizing retention spend?

✔️ How is the highest-risk customer segment defined by combining demographics and geography?

---

## 📂 Dataset Description & Data Structure

### **📌 Data Source**

* **Source**: Kaggle
* **File Name:** `Bank_Churn.csv`
* **Source:** Historical data containing customer profiles and transaction details from a bank.
* **Size:** 10,000 records (rows), 13 fields (columns).
* **Objective:** To build a Classification Model to predict the **Exited** field (customer churn).

---

### 📊 **Data Structure & Relationships**  
 
- 📦 **Fact_Bank_Churn** .

<details>
<summary><strong>Table 1: Bank_Churn</strong></summary>

| Column Name | Data Type (Dtype) | Detailed Description | Category |
| :--- | :--- | :--- | :--- |
| **CustomerId** | Integer | Unique identifier for the customer. | ID |
| **Surname** | String | Customer's last name. | ID |
| **CreditScore** | Integer | Individual credit score (Ranging from 300 to 850). | Financial |
| **Geography** | String | Country/Region of residence (France, Spain, Germany). | Demographic |
| **Gender** | String | Customer's gender. | Demographic |
| **Age** | Integer | CustoGenderID`            | Unique identifier for the gender category      |
| `Gender` | Customer's gender                 |

</details>

---

- 🌍 **Dim_Geography** 

<details>
<summary><strong>Table 2:Geography</strong></summary>

| Column Name           | Description                                |
|------------------------|--------------------------------------------|
| `GeographyID`            | Unique identifier for the geography category      |
| `Geography` | Customer's Geography                |   

</details>

---

- 🧾 **Dim_HasCard** 

<details>
<summary><strong>Table 3:HasCard</strong></summary>

| Column Name           | Description                                |
|------------------------|--------------------------------------------|
| `HasCrCardID`            | Unique identifier for the HasCrCardCategory category      |
| `HasCrCardCategory` | Customer's HasCrCardCategory                |   

</details>

---

- 📊 **Dim_IsActiveMember** 

<details>
<summary><strong>Table 4:IsActiveMember</strong></summary>

| Column Name           | Description                                |
|------------------------|--------------------------------------------|
| `IsActiveCategory`            | Customer's IsActiveMember      |
| `IsActiveMemberID` | Unique identifier for the IsActiveMember category ( 0,1 )             |   

</details>

---

- ⚠️ **Dim_Exited** 

<details>
<summary><strong>Table 5:IsExited</strong></summary>

| Column Name           | Description                                |
|------------------------|--------------------------------------------|
| `ExitedCategory`            | Customer's IsExited      |
| `ExitedID` | Unique identifier for the exited category ( 0,1 )             |   

</details>

---

**OverView**
<img width="1430" height="797" alt="image" src="https://github.com/user-attachments/assets/307bd233-b9d5-4cc3-a262-e136500fcbb6" />

**Risk Impact Analysis**
<img width="1416" height="809" alt="image" src="https://github.com/user-attachments/assets/144999e7-2538-416f-aeb0-c080918c7cf7" />

**Insight**

Customer Demographics
Total customers: 10,000.
Gender: 55% male, 45% female.
Geography: France has the largest customer base, followed by Germany and Spain.

Customer Activity & Product Usage
Active customers: 51%.
Credit card ownership: 70%.
Product usage: Product 1 is most popular, followed by Products 2, 3, and 4.
 Churn Overview

Overall churn rate: 20,37 %
Gender breakdown: 55% of churners are female
Credit card ownership among churners: 70%
Activity status among churners: 63% are inactive
Churn Drivers

Credit Score:
<400 → churn rate = 100%
≥400 → churn rate ~19–21%	

Income:
Very high income (>150k/year) → highest churn (22%)
Middle income (50–100k/year) → lowest churn (20%)

Age:
Middle-aged (40–59) → churn rate 37% (highest)
Teenagers (<20) → churn rate 6% (lowest)
Product Usage:

Products 3 & 4 → significantly higher churn

**Suggestions for The Bank Should Doing**

Credit Card Offerings:
With 70% customer adoption, credit card products are a proven strength. The bank should maintain strong promotion of these offerings and consider introducing tiered benefit packages to serve different customer segments more effectively.

Product 1 & Product 2 Engagement:
Product 1: Highest usage, proving strong alignment with customer needs. Continue enhancing and promoting this product to sustain engagement and satisfaction.
Product 2: Lowest churn rate among all products. Expanding its reach to a broader base could help further reduce overall churn.

Middle-Income Customer Retention:
Middle-income customers (churn rate 20%, lowest among income groups) are well-served by current offerings. The bank should continue strengthening its value proposition for this segment to ensure loyalty and long-term retention.
