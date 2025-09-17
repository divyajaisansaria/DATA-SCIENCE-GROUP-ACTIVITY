
# **Telco Customer Churn Prediction Project – Group Submission**

---

## **Member 1(Neel Patel): Data Loading & Cleaning**

**Steps & Contributions:**

1. **Data Loading:**

   * Loaded Telco Customer Churn dataset directly in Colab via URL.
   * Verified integrity: no duplicates, checked missing values.

2. **Data Cleaning:**

   * Converted `TotalCharges` from object → float.
   * Dropped 11 rows with invalid TotalCharges.
   * Ensured all numeric columns were correctly typed.

**Learning Outcome:**

* Learned how to handle raw data, check for inconsistencies, and prepare it for analysis.

---

## **Member 2(Shashank Maurya): Exploratory Data Analysis (EDA) & Hypothesis Testing**

**Steps & Contributions:**

1. **EDA:**

   * Visualized churn distribution, churn by contract type, tenure, monthly charges.
   * Observed patterns:

     * Month-to-month contracts churn more.
     * High monthly charges → higher churn.
     * Shorter tenure → higher churn.

2. **Hypothesis Testing:**

   * Chi-square test: Contract type significantly affects churn (p ≈ 0).
   * t-tests: Tenure & MonthlyCharges differ significantly between churned vs non-churned customers.

**Learning Outcome:**

* Practiced statistical reasoning and validated insights with hypothesis testing.

---

## **Member 3 & 4(Suhani Acharya & Divya Jaisansaria): Feature Engineering & Model Training**

**Steps & Contributions:**

1. **Feature Engineering:**

   * Dropped `customerID`.
   * Converted target `Churn` to numeric 0/1.
   * One-hot encoded categorical variables.
   * Scaled numeric features: `tenure`, `MonthlyCharges`, `TotalCharges`.

2. **Train/Test Split:**

   * 80% training, 20% testing, stratified on churn.

3. **Model Training:**

   * Trained Logistic Regression, Decision Tree, Random Forest, and KNN.
   * Evaluated models with Accuracy, ROC-AUC, Precision, Recall, F1-score.

**Performance Summary:**

| Model               | Accuracy | Recall (Churn) |
| ------------------- | -------- | -------------- |
| Logistic Regression | 0.8045   | 0.57           |
| Decision Tree       | 0.7193   | 0.47           |
| Random Forest       | 0.7896   | 0.52           |
| KNN                 | 0.7619   | 0.58           |

**Learning Outcome:**

* Learned model selection, training, evaluation, and comparison.

---

## **Member 5(Archit Savaliya): Feature Importance & Reporting**

**Steps & Contributions:**

1. **Feature Importance:**

   * Plotted feature importance from Random Forest.
   * Top 5 features affecting churn:

     * Contract Type
     * Monthly Charges
     * Tenure
     * Payment Method
     * Tech Support

2. **Reporting / Insights:**

   * Logistic Regression chosen as best model due to **highest accuracy (80.45%)** and interpretability.
   * Key business insights:

     * Month-to-month customers with high charges are most likely to churn.
     * Tenure inversely related to churn probability.

**Learning Outcome:**

* Learned to interpret model outputs, extract actionable insights, and summarize findings professionally.

---

## **How to Run the Project**

1. Open the `Telco_Churn.ipynb` notebook in Colab.
2. Run all cells sequentially to reproduce results.

---

## **References**

* Dataset: [Kaggle – Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)
* Python Libraries: Pandas, NumPy, Scikit-learn, Seaborn

---
