# ANALYTICS SPEC
## Sales Analytics Dashboard

Dataset:
`data/online_retail_orders_clean.csv`

Each row = one completed order.

Important columns:
- OrderID
- OrderDate
- OrderMonth
- CustomerID
- Country
- TotalQuantity
- DistinctProducts
- LineCount
- OrderValueGBP
- AvgUnitPriceGBP
- MaxUnitPriceGBP

Currency: GBP (£)

## Core NumPy arrays
```python
order_value = df["OrderValueGBP"].to_numpy()
quantity = df["TotalQuantity"].to_numpy()
```

## Required KPIs
```python
total_revenue = np.sum(order_value)
number_of_orders = len(order_value)
mean_order = np.mean(order_value)
median_order = np.median(order_value)
maximum_order = np.max(order_value)
```

Display:
- Total Revenue
- Number of Orders
- Mean Order Value
- Median Order Value
- Maximum Order Value

Mean and Median must be visually adjacent.

## Statistical summary
```python
q1 = np.percentile(order_value, 25)
q2 = np.percentile(order_value, 50)
q3 = np.percentile(order_value, 75)

iqr = q3 - q1

lower_bound = q1 - 1.5 * iqr
upper_bound = q3 + 1.5 * iqr

variance = np.var(order_value)
std_dev = np.std(order_value)
```

High outliers:
```python
high_outlier_mask = order_value > upper_bound
high_outlier_count = np.sum(high_outlier_mask)
high_outlier_percentage = high_outlier_count / len(order_value) * 100
```

Required interpretation:
> An outlier is statistically unusual. It is not automatically an error, fraud, or a value that should be deleted.

## Chart 1 — Monthly Revenue
Business question:
**How is revenue changing over time?**

- Aggregate OrderValueGBP by OrderMonth
- Line chart
- Chronological order
- Show strongest and weakest month
- Do not invent reasons for changes

## Chart 2 — Top Countries by Revenue
Business question:
**Which markets generate the most revenue?**

- Group by Country
- Sum OrderValueGBP
- Top 10
- Horizontal bar chart
- Show top country, revenue, and share of total

## Chart 3 — Order Value Histogram
Business question:
**What does the distribution of customer order values look like?**

- Histogram of OrderValueGBP
- Full Distribution and Main 99% views
- Main 99% is visual only
- Add Mean and Median reference lines
- Explain right-tail / right-skew conceptually
- Do not calculate a skewness formula

## Chart 4 — Order Value Box Plot
Business question:
**How spread out are order values, and which orders are statistically unusual?**

Show:
- Q1
- Median
- Q3
- IQR
- Upper Bound
- High Outlier Count

Required message:
> Outlier does not mean bad data.

## Chart 5 — Quantity vs Order Value
Business question:
**Do orders containing more units tend to have higher order values?**

X: TotalQuantity  
Y: OrderValueGBP

Covariance:
```python
covariance_matrix = np.cov(quantity, order_value)
covariance = covariance_matrix[0, 1]
```

Interpret as:
- Positive
- Negative
- Near zero

Required warning:
> Covariance does not prove causation.

## Insight panel
Title:
**What the Data Is Telling Us**

Required cards:
1. Typical Order
2. Distribution
3. Unusual Orders
4. Strongest Month
5. Top Market
6. Quantity vs Order Value

Never fabricate causal explanations.

## Optional filters
Allowed:
- Date range
- Country
- Distribution view

Keep filters minimal.

## Validation
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
- High Outlier Count
- Covariance
- Monthly Revenue ordering
- Top Countries
- 99% views do not affect underlying calculations
