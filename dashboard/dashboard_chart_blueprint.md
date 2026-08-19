# Dashboard Chart Blueprint

## Purpose
The dashboard should not merely display charts. Each chart must reinforce a descriptive-statistics concept from the class and answer a business question.

## KPI row
- Total Revenue
- Number of Orders
- Mean Order Value
- Median Order Value
- Maximum Order Value

## Statistical summary strip
- Q1
- Median / Q2
- Q3
- IQR
- Upper Outlier Bound
- High Outlier Count

## 1. Monthly Revenue — Line Chart
**Business question:** How is revenue changing over time?  
**What students learn:** A line chart is appropriate when order/time matters.  
**Dashboard interpretation:** Highlight strongest and weakest month; do not invent causes.

## 2. Top 10 Countries by Revenue — Horizontal Bar Chart
**Business question:** Which markets contribute the most revenue?  
**What students learn:** Bar charts compare categories and rankings.  
**Dashboard interpretation:** Show ranking and revenue concentration.

## 3. Order Value Distribution — Histogram
**Business question:** What does a typical order distribution look like?  
**What students learn:** Bins, frequency, right skew, Mean vs Median.  
**Dashboard interpretation:** Keep all data for statistics, but offer a 99th-percentile visual zoom.

## 4. Order Value — Box Plot
**Business question:** How spread out are order values and which orders are statistically unusual?  
**What students learn:** Median, Q1, Q3, IQR, whiskers, outliers.  
**Dashboard interpretation:** Explain that an outlier is not automatically an error.

## 5. Total Quantity vs Order Value — Scatter Plot
**Business question:** Do larger baskets tend to generate larger order values?  
**What students learn:** Direction of relationship and covariance.  
**Dashboard interpretation:** State the covariance sign and remind users that covariance is not causation.

## Required narrative panel
The dashboard should dynamically answer:
1. Is Mean larger than Median?
2. What does that say about the distribution?
3. How many orders are above the IQR upper bound?
4. Which month has the highest revenue?
5. Which country has the highest revenue?
6. Is Quantity–Order Value covariance positive or negative?

## Teaching principle
**Statistic → Chart → Interpretation → Business decision**