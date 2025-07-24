# Home Equity Line of Credit (Loan Default Prediction and Analysis)

This project is focused on analyzing and predicting loan default risk using data from Home Equity Line of Credit (HELOC) applications. It combines visual analytics in **Power BI** with **machine learning** using Python’s XGBoost to uncover key insights and support decision-making for credit risk management.

## Project Overview

Lending institutions face significant risks when borrowers default on loans. This analysis aims to:
- Understand the patterns and characteristics associated with defaulting.
- Identify high-risk borrower profiles.
- Use machine learning (XGBoost) to predict the likelihood of default.
- Support data-driven decisions on loan approval, interest rates, and risk mitigation.

---

## Dataset Overview

The dataset contains 10,000 records and includes the following key fields:

| Feature        | Description |
|----------------|-------------|
| `DEBTINC`      | Debt-to-income ratio |
| `CLAGE`        | Age of the oldest trade line |
| `MORTDUE`      | Amount due on existing mortgage |
| `VALUE`        | Value of current property |
| `LOAN`         | Amount of the requested loan |
| `CLNO`         | Number of credit lines |
| `YOJ`          | Years on the current job |
| `JOB`          | Occupation type |
| `DELINQ`       | Number of past delinquencies |
| `DEFAULT`      | Target variable (1 = default, 0 = no default) |

---


## Key Insights from Power BI

1. **Default Rate:**  
   The overall default rate was found to be relatively moderate, but varies significantly across segments.

2. **Loan Reason:**  
   Borrowers who took loans for **debt consolidation** defaulted more than those who applied for **home improvement** loans.

3. **Years on Job:**  
   There’s a U-shaped pattern: those with **very short** or **very long** years on the job had higher default rates than those in mid-career (6–15 years).

4. **Job Type:**  
   Default rate was higher among job categories like *Other*, *Sales*, and *Laborers*. Professionals and Managers defaulted less.

---

## Machine Learning - XGBoost Model

An XGBoost model was trained to identify feature importance for predicting loan default.

### Feature Importance Ranking

| Feature   | Importance Score |
|-----------|------------------|
| DEBTINC   | 320              |
| CLAGE     | 319              |
| MORTDUE   | 296              |
| VALUE     | 281              |
| LOAN      | 262              |
| CLNO      | 237              |
| YOJ       | 197              |
| JOB       | 111              |
| DELINQ    | 92               |

### Insights from Feature Importance

- **Debt-to-Income Ratio (DEBTINC)** is the most influential feature. Borrowers with high debt relative to income are far more likely to default.
- **Age of Oldest Credit Line (CLAGE)** is critical — a longer credit history is linked to more responsible borrowing behavior.
- **Mortgage Due (MORTDUE)** and **Property Value (VALUE)** also play key roles, showing the importance of collateral and existing liabilities.
- Surprisingly, **Past Delinquencies (DELINQ)** had the lowest impact in this dataset, likely due to low variance or missing data.
- **Job** and **Years on Job (YOJ)** matter less to the model but are still valuable for manual risk assessment.

---

## Recommendations

1. **Tighten Approval Criteria for High DEBTINC Applicants:**  
   Consider setting stricter approval limits or offering lower amounts to applicants with high debt-to-income ratios.

2. **Reward Long Credit Histories:**  
   Offer better terms to borrowers with longer credit histories (high CLAGE), as they demonstrate financial maturity.

3. **Segment Loan Offers by Occupation Type:**  
   Offer custom risk-based pricing or require additional checks for higher-risk professions.

4. **Focus on Mid-Career Borrowers (YOJ 6–15):**  
   Target loans to borrowers with a stable career length, as they are less likely to default.

5. **Balance Loan Amount with Property Value:**  
   Always ensure that loan amounts don’t significantly exceed the property value to reduce exposure.

6. **Combine ML Predictions with Business Rules:**  
   Use the model’s prediction alongside manual evaluations to reduce false positives or missed risks.

---

## Tools & Technologies

- **Power BI** – for interactive data visualization.
- **Python (XGBoost)** – for machine learning modeling.
- **Pandas, Matplotlib, Sklearn** – for data processing and evaluation.


---

## Future Improvements

- Include more recent and diverse loan data.
- Add SHAP analysis for better feature explainability.
- Integrate Power BI report with live dashboards via Power BI service or embedded links.
- Automate model training and refresh with updated datasets.

---

## Acknowledgements

Thanks to the open-source community for tools like Power BI, Python, and the scikit-learn ecosystem. Inspired by real-world challenges in financial data analytics.

---

## Contact

For collaborations or questions, reach out on [LinkedIn](https://www.linkedin.com/in/gideon-aleji-4b7073354/) or [email@example.com](mailto:alejigideonabidemi@gmail.com).




