# MASTER CURSOR PROMPT
## Guided Vibe Coding — Sales Analytics Dashboard

You are joining an existing classroom Data Science project as a senior analytics product engineer.

Do not start coding immediately.

## Project structure

```text
end-to-end-analytics-projects/
├── context/
│   ├── PRODUCT_BRIEF.md
│   ├── ANALYTICS_SPEC.md
│   └── DESIGN_SYSTEM.md
├── data/
│   └── online_retail_orders_clean.csv
├── notebook/
│   └── sales_analytics_lab_complete.ipynb
├── dashboard/
├── requirements.txt
└── ...
```

## Step 1 — Read before coding

Read completely:
1. `context/PRODUCT_BRIEF.md`
2. `context/ANALYTICS_SPEC.md`
3. `context/DESIGN_SYSTEM.md`

Then inspect:
4. `data/online_retail_orders_clean.csv`
5. `notebook/sales_analytics_lab_complete.ipynb`
6. `requirements.txt`

The notebook is the analytical reference.
The context files are the product, analytics, and design source of truth.

If anything conflicts, flag it before changing files.

## Step 2 — Do NOT build the dashboard yet

Before writing code, respond with:

### A. Product understanding
- primary user
- main business questions
- out-of-scope items

### B. Analytics understanding
- required KPIs
- required statistics
- required charts
- required insights

### C. Design understanding
- visual direction
- page hierarchy
- chart layout
- projector-readability requirements

### D. Proposed Streamlit architecture
Explain:
- data loading
- robust path strategy
- helper functions
- page sections
- Plotly organization
- CSS strategy
- validation strategy

Keep the architecture beginner-readable.

### E. Implementation sequence
Propose a phased build.

Do not create or modify files yet.

STOP after the summary and plan.
Wait for my approval.

---

# Implementation phases

## PHASE 1 — App shell
When approved:
Create/update `dashboard/app.py`.

Implement only:
- imports
- page config
- robust project-root paths
- cached CSV loading
- main NumPy arrays
- compact header
- empty section containers
- dark visual foundation

Verify app startup.

## PHASE 2 — KPI + statistics
Implement:
- Total Revenue
- Orders
- Mean
- Median
- Maximum
- Q1/Q2/Q3
- IQR
- Std Dev
- Upper Bound

Mean and Median adjacent.

Validate numbers.

## PHASE 3 — Monthly Revenue
Implement only Monthly Revenue.
Use Plotly.
Treat it as hero chart.
Do not add other charts yet.

## PHASE 4 — Distribution
Implement:
- Histogram
- Mean line
- Median line
- Full / Main 99% control
- skewness interpretation

Then:
- Box Plot
- Q1/Median/Q3/IQR/Upper Bound
- High Outlier Count
- “Outlier ≠ bad data”

Do not remove outliers.

## PHASE 5 — Markets + relationship
Implement:
- Top 10 Countries horizontal bars
- top market share

Then:
- Basket Size vs Order Value scatter
- covariance
- covariance direction
- Full / Main 99% view
- causation warning

## PHASE 6 — Insight layer
Build:
**What the Data Is Telling Us**

Six dynamic cards:
- Typical Order
- Distribution
- Unusual Orders
- Strongest Month
- Top Market
- Quantity vs Order Value

Only use supported data.

## PHASE 7 — Design QA
Do not add features.

Act as a senior product designer.
Review:
- hierarchy
- spacing
- typography
- projector readability
- chart readability
- default Streamlit feel
- unnecessary noise
- responsive layout

First provide critique only.
Do not modify code until approved.

## PHASE 8 — Analytics QA
Act as a data analyst.
Do not redesign UI.

Validate:
- Total Revenue
- Orders
- Mean
- Median
- Q1/Q2/Q3
- IQR
- Variance
- Standard Deviation
- Bounds
- Outlier Count
- Covariance
- strongest month
- top country
- top-country share

Confirm 99% views do not alter statistics.

## PHASE 9 — Final technical validation
Check:
- app starts
- imports work
- project-root paths work
- Plotly charts render
- layout renders
- filters do not break metrics
- requirements are sufficient
- no fake data exists

Update `requirements.txt` only if needed.

---

# Permanent constraints

- Use Streamlit + Plotly + Pandas + NumPy.
- Keep Python readable for beginners.
- Do not introduce advanced Data Science.
- Do not invent data.
- Do not remove outliers.
- 99% zoom is visual only.
- Every chart needs a business question.
- No pie charts.
- No gauges.
- Minimal filters.
- Do not over-engineer.
- Do not change analytics while polishing UI unless a real bug exists.

# Start now

Read the context, dataset, notebook, and requirements.

Then provide only:
1. Product understanding
2. Analytics understanding
3. Design understanding
4. Proposed Streamlit architecture
5. Implementation sequence

Do not write code yet.
