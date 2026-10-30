# Initial EDA Plan (Week 2)

## Target (no leakage)
Reference date T; predictors from data before T only. Label = ≥1 purchase in (T, T+W]. Run a sensitivity check with a second window. Exclude customers whose window extends past the end of the data. Use a time-based train/test split.

## Hypotheses → data → methods
| ID | Variables | Sources | Method | Visual |
|---|---|---|---|---|
| H1 | past orders, repeat label | S1, S2, S3 | Mann–Whitney U; logistic regression; ROC-AUC vs baseline | Boxplot; repeat rate by frequency band |
| H2 | category, repeat label | S1, S2, S3 | Chi-square + Cramér's V; multiple-comparison correction | Bar chart with Wilson intervals |
| H3 | days since last purchase, time to next purchase | S1, S2, S3 | Kaplan–Meier; logistic regression; Mann–Whitney U | Gap histogram; survival curve |
| RQ1 | orders per customer, order value | S1–S3 | Descriptive statistics | Log-scale histograms |
| RQ4 | missingness, duplicates, bias | all | Data-quality report | Missingness heatmap |

Results are associations only, not causal claims.
