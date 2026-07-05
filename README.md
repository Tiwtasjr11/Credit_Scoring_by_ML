# Credit Scoring Project

## 📌 Project Overview
This project aims to build a **Credit Scoring Model** to predict the likelihood of a customer defaulting on a loan (identifying 'Good' vs. 'Bad' loans). By analyzing historical customer data such as age, income, employment length, and loan details, the model helps in assessing the creditworthiness of applicants.

## 💡 Benefits
* **Risk Mitigation:** Helps financial institutions minimize losses by identifying high-risk borrowers before approving loans.
* **Automated Decision Making:** Speeds up the loan approval process by providing data-driven recommendations.
* **Fairness and Consistency:** Reduces human bias in credit evaluation by relying on objective statistical criteria.

## ⚠️ Important Considerations: Variance Inflation Factor (VIF)
When building regression models (like Logistic Regression, which is common in credit scoring), it is crucial to check for multicollinearity among the independent variables. High multicollinearity can make the model unstable and inflate the standard errors of the coefficients.

We measure this using the **Variance Inflation Factor (VIF)**. 

**VIF Equation:**
VIF_i = \frac{1}{1 - R_i^2}
*Where R_i^2 is the R-squared value obtained by regressing the i^{th} independent variable against all other independent variables.*

* **Rule of Thumb:** A VIF value greater than 5 (or sometimes 10) indicates problematic multicollinearity, suggesting that the variable should be investigated and potentially removed from the model.

## 🛠️ Step-by-Step Process (Based on the Notebook)
1. **Import Libraries & Load Dataset:** Importing essential tools (`pandas`, `numpy`, `matplotlib`, `seaborn`) and loading the customer credit data.
2. **Data Exploration:** Checking data shape, data types, and initial rows to understand the structure.
3. **Univariate Analysis (Target Variable):** * Defining the target variable (`loan_status` as 'Good' or 'Bad').
   * Calculating the Imbalance Ratio (IR) to understand the distribution of classes.
   * Visualizing the target distribution using count plots.
4. **Descriptive Statistics:** Summarizing numerical features (mean, std, min, max, etc.).
5. **Feature Distribution Visualization:** Plotting distributions of individual features (e.g., `person_age`, `person_income`) to identify patterns and potential outliers.
6. **(Further typical steps inferred):** Data preprocessing, model training, evaluation, and cutoff selection (as hinted by the final output snippet).
