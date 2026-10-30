# Analysis Plan

*Planning document – no analysis has been performed yet.*

## Step 1 – Define the prediction target
Specify what counts as a repeat purchase and the future window (e.g. another order within N days after a reference date). Choose the window using the data and business context.

## Step 2 – Obtain and understand the data
Review source, field definitions, observation period, coverage, licence and limitations. Use only data that can be accessed and used appropriately.

## Step 3 – Clean and prepare
Check missing values, duplicates, data types, dates, inconsistent categories and implausible values. Document all exclusions and transformations.

## Step 4 – Exploratory data analysis
Summarise customer counts, purchase frequency, order amounts, categories and timing using tables and charts.

## Step 5 – Feature creation
If supported: past purchase count, total past spending, average order amount, days since last purchase. Use only information available at the prediction date (avoid data leakage).

## Step 6 – Baseline
Start with a simple baseline (e.g. majority class). Use a time-based split so future data is not used to predict the past.

## Step 7 – Model (optional)
If a reliable label exists, try logistic regression or a decision tree.

## Step 8 – Evaluation
Use metrics suited to class balance and business cost: precision, recall, F1, ROC-AUC.

## Step 9 – Business ideas
If supported by evidence, propose reminders / product information / retention campaigns. A controlled experiment is needed to show causal impact.

## Deliverables
Problem statement, source review, data dictionary, data-quality checklist, EDA plan, feasibility recommendation. In a later phase (if data is suitable): EDA notebook, baseline comparison, evaluation metrics, labelled visualisations.

## Success criteria (Week 1)
The problem is specific, the research questions are answerable, candidate variables and sources are identified, and the method is coherent and realistic. This does **not** mean a model has been built or validated.
