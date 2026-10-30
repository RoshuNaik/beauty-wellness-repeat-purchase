# Predicting Customer Repeat Purchases in the Beauty & Wellness Industry

**Data Science – Week 1: Orientation and Problem Definition**
Author: Roshan Jadhav

> **Project status:** Problem definition and planning stage. No dataset has been analysed yet and no model has been trained. This repository contains no results or business-impact claims.

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
│   ├── Week1_Beauty_Wellness_Data_Science_Report.docx   # full report
│   ├── analysis_plan.md
│   ├── data_dictionary.md
│   ├── data_quality_checklist.md
│   └── references.md
├── data/            # raw data is NOT committed (see data/README.md)
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

- [ ] Verify and select a dataset (licence, access, fields)
- [ ] Define "repeat purchase" and the prediction window
- [ ] Complete the data-quality checklist
- [ ] Perform EDA in `notebooks/`
- [ ] Decide whether prediction is feasible
