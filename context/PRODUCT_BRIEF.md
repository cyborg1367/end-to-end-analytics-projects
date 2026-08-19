# PRODUCT BRIEF
## Sales Analytics Dashboard — Intro to Data Science

### Purpose
Build an interactive sales analytics dashboard for an introductory Data Science classroom project.

Class flow:
**Real Sales Data → Descriptive Statistics → Visualization → Interpretation → Business Dashboard**

### Primary user
A business manager who should understand the business in under 60 seconds.

The dashboard should answer:
- How much revenue did the company generate?
- How many orders were completed?
- What does a typical order look like?
- Is Mean representative of most orders?
- Are there statistically unusual high-value orders?
- How does revenue change over time?
- Which countries generate the most revenue?
- Do larger baskets tend to generate larger order values?

### Secondary user
Beginner Data Science students.

Concepts already covered:
- Mean, Median, Mode
- Variance, Standard Deviation
- Covariance
- Histogram, Box Plot
- Q1, Q2, Q3, Percentiles
- IQR and outlier bounds
- Conceptual Skewness
- NumPy arrays, aggregation, slicing, masking

### Scope boundary
This is NOT an advanced EDA project.

Do not introduce:
- regression
- machine learning
- forecasting
- clustering
- hypothesis testing
- advanced anomaly detection
- complex cleaning workflows

### Technology
Use:
- Python
- Streamlit
- Pandas
- NumPy
- Plotly

Main app:
`dashboard/app.py`

Dataset:
`data/online_retail_orders_clean.csv`

Notebook:
`notebook/sales_analytics_lab_complete.ipynb`

Run from project root:
`streamlit run dashboard/app.py`

### Product personality
The dashboard should feel:
- professional
- calm
- analytical
- modern
- executive
- high contrast
- projector friendly

Avoid:
- default Streamlit demo look
- colorful student-project styling
- decorative dashboard templates
- excessive animations
- excessive emojis

### Data integrity
Never invent numbers.

Every KPI, chart, percentile, bound, covariance value, and insight must come from the real CSV.

Outliers are intentionally kept.
Do not remove outliers from calculations.

Main 99% views are allowed only as visual zooms.

### Core principle
Every visual must answer either:
1. What business question does this answer?
2. What Data Science concept does this reinforce?

Final story:
**Summary → Trend → Distribution → Unusual Orders → Market Ranking → Relationship → Insights**
