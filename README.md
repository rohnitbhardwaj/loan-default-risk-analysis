# Loan Default Risk Analysis

**Python · Power BI · Statistics**

📊 **[View Dashboard Screenshots]([images/](https://github.com/rohnitbhardwaj/loan-default-risk-analysis/tree/main/images))**

## Business Problem

Which loans are most likely to default, and which segments account for
the greatest financial losses? The goal is to help lenders identify higher-risk segments and review their risk assessment and pricing strategies.

## Dataset

Lending Club loan data (2007--2011). After excluding loans still in
progress, the analysis covers **38,577 completed loans**, including
**5,627 defaults (14.6%)**.

[Dataset source --
Kaggle](https://www.kaggle.com/datasets/tanishaj225/loancsv)

## Methodology

1.  **Dataset:** defined default as "Charged Off" and excluded loans still in progress.
2.  **Transformation (Python):** removed empty and data-leakage columns, converted text fields to numbers, fixed dates, and grouped values into bands (income, DTI, loan amount, interest rate).
3.  **Analysis (Python):** Analysed default rates by segment using confidence intervals, Chi-square tests with Cramér's V, Mann-Whitney U tests, relative risk and Spearman correlation.
4.  **Visualization (Power BI):** a 2-page dashboard with DAX measures and filters: who defaults and where the money is lost.

## Key Findings

-   **Loan grade:** Default rates rise from approximately **6% (Grade A)
    to 34% (Grade G)**. Grade and interest rate are the strongest,
    closely related risk indicators.
-   **Loan term:** 60-month loans default at **25%**, versus **11%** for
    36-month loans. They represent about **25% of loans but 59% of
    principal losses**.
-   **Loan purpose:** Small business loans have the highest default rate
    (**27%**), while debt consolidation accounts for about **55% of
    dollars lost** due to its high loan volume.
-   **Loan size:** Larger loans appear riskier largely because they are
    concentrated in lower grades.
-   **Overall losses:** Approximately **10.3% of funded principal** was
    charged off.

## Recommendations

-   Review risk assessment and pricing for lower-grade loans.
-   Monitor 60-month loans, particularly in lower grades.
-   Apply additional assessment to small business applications.
-   Prioritise segments using both default rates and total financial
    exposure.

## Limitations

-   Covers issued loans from 2007--2011; findings may not reflect
    current lending conditions.
-   Excluding loans still in progress may overstate the 60-month default
    gap.
-   Charged-off principal excludes later recoveries.
-   Small categories have too few observations for reliable conclusions.

## Project Files

-   `loan_default_analysis.ipynb` -- Python analysis
-   `loan_clean.csv` -- Cleaned dataset
-   `loan_default_dashboard.pbix` -- Power BI dashboard
-   `images/` -- Dashboard screenshots

---

**Rohnit Bhardwaj**
