# Customer Spend Hypothesis Testing

Statistical analysis of a US customer dataset (10,675 records) using formal hypothesis testing to determine which demographic and behavioral factors *actually* drive differences in monthly spending, engagement, and pet ownership — rather than relying on visual inspection of charts alone.

## 📌 Overview

Most "data analysis" projects stop at charts and summary statistics. This project goes one step further: for every business question, a specific statistical hypothesis test was chosen, run, and interpreted using p-values — separating patterns that are statistically real from ones that just look interesting in a plot.

## 📊 Dataset

**US Customer Insights Dataset**
- 10,675 customers
- 12 features: `CustomerID`, `Name`, `State`, `Education`, `Gender`, `Age`, `Married`, `NumPets`, `JoinDate`, `TransactionDate`, `MonthlySpend`, `DaysSinceLastInteraction`

## 🔬 Business Questions & Methodology

| # | Business Question | Statistical Test | Result (p-value) | Conclusion |
|---|---|---|---|---|
| 1 | Do male and female customers differ in average monthly spend? | Independent Two-Sample t-test | p = 0.73 | ❌ No significant difference |
| 2 | Does education level impact average monthly spend? | One-Way ANOVA | p = 0.92 | ❌ No significant difference |
| 3 | Is customer age related to engagement (days since last interaction)? | Pearson Correlation | p = 0.68 | ❌ No significant relationship |
| 4 | Does average monthly spend differ across states? | One-Way ANOVA | p = 0.35 | ❌ No significant difference |
| 5 | Is marital status related to number of pets owned? | Chi-square Test | p ≈ 2.4 × 10⁻³⁷ | ✅ Highly significant relationship |

## 🔑 Key Findings

- **Marital status strongly predicts pet ownership** — the only statistically significant result across all 5 tests, pointing to a genuine lifestyle difference between married and unmarried customers.
- **Monthly spending is remarkably uniform** — gender, education level, and state show no statistically significant effect on how much customers spend, despite visible-looking differences in raw averages. This is a useful finding in itself: it tells a business *where not* to over-segment marketing spend.
- **Age has no measurable link to customer engagement** — older and younger customers interact with the business at similar frequency.

## 🛠️ Tools & Techniques

- **Language:** Python
- **Libraries:** Pandas, NumPy, SciPy (`ttest_ind`, `f_oneway`, `chi2_contingency`, `pearsonr`), Matplotlib, Seaborn
- **Techniques:** Exploratory Data Analysis (EDA), Data Cleaning, Independent t-test, One-Way ANOVA, Chi-square Test of Independence, Pearson Correlation, Hypothesis Testing (H₀ / H₁ framework, p-value interpretation)

## 📁 Project Structure
├── Statistics_Mini_Project.ipynb     # Full analysis notebook
├── US_Customer_Insights_Dataset.csv  # Raw dataset
└── README.md

## 🚀 How to Run

```bash
pip install pandas numpy scipy matplotlib seaborn
jupyter notebook Statistics_Mini_Project.ipynb
```

## 💡 Takeaway

Statistical significance testing prevents drawing wrong conclusions from visually "interesting" but random differences in data. Out of 5 hypotheses tested, only 1 held up — a reminder that rigorous testing matters more than eyeballing charts when making business decisions.

## 👤 Author

Rushabh Upadhye
Data Analyst | SQL, Excel, Power BI, Python, Statistics, Machine Learning
📍 Open to Data Analyst roles 
