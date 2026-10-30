# Data Cleaning and Preprocessing Plan (Week 2)

| Issue | Planned action |
|---|---|
| Duplicate records | Remove exact duplicate order rows; flag repeated identical events |
| Missing category (S1, S2) | Map via category_id / title keywords, else "unknown"; never guess |
| Event types (S1) | Purchase events for the label; view/cart only as optional features |
| Dates / time zones | Parse, unify time zone, remove impossible dates |
| Price / quantity outliers | Inspect first; log-scale plots; remove only clear errors and log why |
| Gift cards (S2) | Exclude from frequency counts |
| Category vs title mismatch (S2) | Beauty filter from category + keywords; manual sample review |
| Cancelled orders (S3) | Keep completed orders only |
| Text fields | Lowercase, trim, standardise brand/category |
| Atypical users | Flag possible bots; compare results with/without |
| Left censoring | First observed order is not necessarily the first ever |
| Class imbalance | Report balance; use precision/recall/F1/ROC-AUC |
| Privacy | Pseudonymous IDs; no cross-dataset linking |
