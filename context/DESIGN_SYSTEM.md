# DESIGN SYSTEM
## Dark Executive Analytics

### Visual direction
Style:
**Dark Executive Analytics**

Keywords:
- calm
- editorial
- precise
- data-first
- premium
- modern
- minimal
- high contrast
- projector friendly

Avoid:
- default Streamlit styling
- excessive gradients
- rainbow charts
- glassmorphism everywhere
- giant decorative hero sections
- excessive emojis
- unnecessary animations
- pie charts
- gauge charts
- visual clutter

### Color system
```text
Page Background     #07111A
Primary Surface     #0E1C28
Raised Surface      #142636
Border              rgba(255,255,255,0.08)

Primary Text        #F4F8FB
Secondary Text      #9EB0BF

Primary Accent      #64DBC8
Secondary Accent    #7EA6FF
Warning             #F6BD60
Outlier / Alert     #FF7E8F
```

### Page hierarchy
Recommended flow:
```text
Header
↓
KPI Row
↓
Statistical Summary Strip
↓
Monthly Revenue — Hero Chart
↓
Histogram + Box Plot
↓
Top Countries + Scatter Plot
↓
What the Data Is Telling Us
↓
Footer
```

### Header
Compact.

Title:
**Sales Analytics Dashboard**

Subtitle:
**Real Online Retail Orders · Intro to Data Science**

Metadata:
**Instructor: Masoud Ahangari**

Avoid a giant hero banner.

### KPI cards
Compact executive cards:
- subtle border
- dark surface
- 14–18px radius
- muted label
- large value
- minimal shadow

Order:
`Total Revenue | Orders | Mean Order | Median Order | Maximum Order`

Mean and Median must be adjacent.

### Statistical strip
Do not create one large card per statistic.

Use:
`Q1 | Median/Q2 | Q3 | IQR | Std Dev | Upper Bound`

### Section pattern
Each chart section should have:
1. Short title
2. One-line business question
3. Chart
4. “How to read this chart” interpretation

Avoid raw database column names in UI.

Bad:
`TotalQuantity vs OrderValueGBP`

Good:
`Basket Size vs Order Value`

### Monthly Revenue
Hero visualization.
- full width
- minimal grid
- clean axes
- readable months
- GBP formatting
- no unnecessary legend

### Histogram
Educational centerpiece.
- clear bins
- Mean line = warning/amber
- Median line = primary/turquoise
- Full / Main 99% view
- conceptual skewness callout

### Box Plot
Pair with:
- Q1
- Median
- Q3
- IQR
- Upper Bound
- High Outlier Count

Message:
**Outlier ≠ bad data**

### Scatter Plot
Title:
**Basket Size vs Order Value**

- small markers
- low opacity
- clean axes
- Main 99% view if needed
- covariance direction
- causation warning

### Top Countries
Horizontal bars.
Country names fully readable.
Top market may use primary accent.

### Insight cards
Section:
**What the Data Is Telling Us**

Six cards:
1. Typical Order
2. Distribution
3. Unusual Orders
4. Strongest Month
5. Top Market
6. Quantity vs Order Value

Each card:
- small label
- short headline/value
- one concise interpretation

### Streamlit styling
Custom CSS through `st.markdown(..., unsafe_allow_html=True)` is allowed.

Use it to:
- reduce default Streamlit feel
- improve spacing
- improve cards
- improve typography

Do not build a fragile custom frontend inside Streamlit.

### Projector readability
- strong contrast
- no tiny labels
- no thin unreadable lines
- restrained legends
- sufficient spacing

### Design rule
Before adding any visual element, complete:
> “This exists because it helps answer ______.”

If the answer is unclear, do not add it.
