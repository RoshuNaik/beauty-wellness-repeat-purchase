# Predicting Customer Repeat Purchases in the Beauty & Wellness Industry

**Data Science – Week 1 (Problem Definition), Week 2 (Data Sourcing Strategy) and Week 3 (Data Cleaning & Preprocessing)**

Author: Roshan Jadhav

> **Project status:** Planning and design stage (Weeks 1–3). No real dataset has been downloaded or analysed, the cleaning pipeline has not been run on real data, and no model has been trained. This repository contains no results or business-impact claims.

## Week 2 – Data sourcing strategy

Ten public sources were reviewed (event logs, purchase histories, review data, product database, government safety data, search trends, open-data portal, social media). Recommended plan: **S1 (REES46 cosmetics events)** and **S2 (Open e-commerce 1.0, beauty subset)** as main datasets, **S3 (Olist)** as a cross-market check, others for enrichment/context. Some source pages could not be opened during the review and are marked *not verified*.

- Full report: [docs/Week2_Data_Sourcing_Strategy_Report.pdf](docs/Week2_Data_Sourcing_Strategy_Report.pdf)
- [Source catalogue](docs/source_catalog.md) · [EDA plan](docs/eda_plan.md) · [Cleaning plan](docs/cleaning_plan.md)

## Week 3 – Data cleaning and preprocessing pipeline

A reproducible Python (pandas + NumPy) workflow for beauty and wellness data (customer, appointment, service, rating and spend fields). Steps: preserve the raw file, inspect, standardise column names and text, remove exact duplicates, convert numbers and dates safely, validate business rules, handle missing values with documented rules (no invented IDs or dates; "Unknown" for categories; median imputation as a baseline), flag outliers with the IQR method instead of deleting them, create Min-Max normalised copies, and export a cleaned CSV plus an audit summary.

> The Week 3 report uses an **illustrative schema** because no raw dataset was supplied. Column names and valid ranges must be confirmed against the real data before running the pipeline. Private customer data must never be uploaded to this public repository.

- Report: [docs/Week3_Data_Cleaning_Preprocessing_Report.docx](docs/Week3_Data_Cleaning_Preprocessing_Report.docx)

## Project question

Can historical customer purchasing behaviour and transaction characteristics help identify customers who are more likely to make a repeat purchase of beauty or personal-care products within a defined future period?

## Why it matters

- **Retention:** repeat-purchase patterns can inform retention strategies.
- **Marketing efficiency:** different customer groups may respond differently to reminders, offers or product information.
- **Customer experience:** relevant communication is more useful than the same message for everyone.
- **Planning:** purchase intervals and categories can help campaign and inventory planning.

These are potential benefits to investigate, not guaranteed outcomes.

## Objectives

1. Understand the structure and quality of a suitable public dataset.
2. Describe purchase frequency, order value, product category and timing (where available).
3. Compare repeat and one-time purchasers (where the data permits).
4. Explore the link between past behaviour and a defined repeat-purchase outcome.
5. Produce a clear, ethical and measurable analysis plan.

## Research questions and hypotheses

| # | Research question |
|---|---|
| RQ1 | How do purchase frequency and order value vary across customers? |
| RQ2 | Are customers with more frequent past purchases more likely to buy again in a defined future window? |
| RQ3 | Do repeat-purchase patterns differ across beauty product categories? |
| RQ4 | What data limitations could affect the reliability of a prediction? |

- **H1:** More frequent past purchases are associated with a higher probability of a repeat purchase.
- **H2:** Repeat-purchase behaviour varies across product categories.
- **H3:** Time since last purchase is associated with the likelihood of another purchase.

Hypotheses are testable assumptions, not established findings. Association does not establish causation.

## Planned methodology

1. Define the prediction target and window
2. Obtain and understand the data (check licence and access)
3. Clean and prepare the data
4. Exploratory data analysis (EDA)
5. Feature creation (only using information available at the prediction date)
6. Baseline (e.g. majority class, time-based split)
7. Optional simple model (logistic regression / decision tree)
8. Responsible evaluation (precision, recall, F1, ROC-AUC)
9. Translate findings into testable business ideas

Details: [docs/analysis_plan.md](docs/analysis_plan.md)

## Candidate data sources (to be verified)

- Kaggle – Cosmetics purchase prediction dataset: https://www.kaggle.com/c/cosmetics/data
- Open e-commerce 1.0 (Scientific Data, 2024): https://www.nature.com/articles/s41597-024-03329-6
- Background study on skincare repurchase intention (Vietnam): https://doi.org/10.1016/j.heliyon.2024.e32285

See [docs/references.md](docs/references.md). Availability, licence and field coverage must be confirmed before use.

## Repository structure

```
.
├── README.md
├── requirements.txt
├── .gitignore
├── docs/
│   ├── Week1_Beauty_Wellness_Data_Science_Report.docx   # Week 1 report
│   ├── Week2_Data_Sourcing_Strategy_Report.pdf / .docx   # Week 2 report
│   ├── Week3_Data_Cleaning_Preprocessing_Report.docx    # Week 3 report
│   ├── source_catalog.md
│   ├── eda_plan.md
│   ├── cleaning_plan.md
│   ├── analysis_plan.md
│   ├── data_dictionary.md
│   ├── data_quality_checklist.md
│   └── references.md
├── data/            # raw/interim/processed – data is NOT committed (see data/README.md)
├── notebooks/       # EDA notebooks (next phase)
└── src/             # scripts (next phase)
```

## Ethics, privacy and limitations

- Use only public or authorised data and follow its licence.
- Do not try to identify individuals; use pseudonymous IDs.
- Check sample bias and missing fields; public data may not represent the Indian market.
- Do not make unsupported claims about individual customers.
- Document assumptions and methods for reproducibility.

## Next steps

- [ ] Open S1, S2, S3 pages; confirm licence, files and size
- [ ] Download and profile the real data
- [ ] Map real column names and run the cleaning pipeline; add the cleaning summary
- [ ] Define "repeat purchase" and the prediction window
- [ ] Complete the data-quality checklist
- [ ] Perform EDA in `notebooks/`
- [ ] Decide whether prediction is feasible
