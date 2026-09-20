# Blinkit Sales Analysis | Power BI

An interactive Power BI dashboard that analyzes Blinkit grocery sales across product categories, outlet characteristics, locations, and establishment years. The project covers data preparation in Power Query, DAX-based KPI development, interactive reporting, and business-oriented analysis.

![Dashboard Preview](Power-BI/dashboard.pg)

## Business Objective

Understand how sales vary across product and outlet dimensions, and provide an interactive dashboard for exploring the factors associated with that variation.

The analysis covers:

- Overall sales performance
- Product category performance
- Fat content distribution
- Outlet size, location, and type performance
- Sales trends by outlet establishment year
- Customer ratings

## Key Performance Indicators

| KPI | Value |
|---|---|
| Total Sales | $1.20M |
| Average Sales | $141 |
| Number of Items | 8,523 |
| Average Rating | 3.9 |

## Dataset

The dataset contains approximately 8,523 records and 12 attributes covering products, sales, ratings, and outlet characteristics.

**Main attributes:** Item Identifier, Item Fat Content, Item Type, Item Weight, Item Visibility, Sales, Customer Rating, Outlet Identifier, Outlet Establishment Year, Outlet Location Type, Outlet Size, Outlet Type

## Data Preparation

Data was cleaned in Power Query before building the report. Key steps:

- Standardized inconsistent values in Item Fat Content (`LF` → `Low Fat`, `REG` → `Regular`)
- Corrected inconsistent capitalization
- Checked categorical fields for missing or invalid values
- Reviewed numerical fields for data-quality issues
- Kept all Power Query transformation steps documented

## DAX Measures

```DAX
Total Sales = SUM(BlinkitData[Sales])

Average Sales = AVERAGE(BlinkitData[Sales])

Number of Items = COUNTROWS(BlinkitData)

Average Rating = AVERAGE(BlinkitData[Rating])
```

Field Parameters let users switch between key metrics within selected visuals.

## Dashboard Analysis

- **Sales by Fat Content:** compares sales contribution from Low Fat and Regular products.
- **Sales by Item Type:** analyzes sales across categories such as Fruits and Vegetables, Snack Foods, Household, Frozen Foods, and Dairy.
- **Fat Content by Outlet:** shows the contribution of each fat-content category across outlet locations.
- **Outlet Establishment Trend:** shows how sales vary by establishment year across outlet generations.
- **Outlet Size:** compares Small, Medium, and High-sized outlets.
- **Outlet Location:** compares Tier 1, Tier 2, and Tier 3 locations.
- **Outlet Type:** KPI-level comparison using Total Sales, Number of Items, Average Sales, Average Rating, and Item Visibility.

## Key Findings

- Total sales are approximately $1.20M, with average sales of approximately $141.
- Low Fat products account for a larger share of sales than Regular products.
- Tier 3 outlets contribute higher total sales than Tier 1 and Tier 2 outlets.
- Fruits and Vegetables and Snack Foods are among the highest-selling categories.
- Sales vary considerably by establishment year, with the 2018 cohort showing a notable peak.
- Medium-sized outlets account for a substantial share of sales.
- The average customer rating is approximately 3.9.

> These findings describe the available dataset only and do not establish causal relationships between outlet or product characteristics and sales.

## Business Recommendations

- Prioritize Tier 3 outlets and the Fruits and Vegetables and Snack Foods categories, since they drive the most sales.
- Look into what made the 2018 outlet cohort perform so strongly and whether it can be replicated.
- Review the Regular product range, since it contributes less than Low Fat.

## Dashboard Features

- Interactive KPI cards
- Dynamic metric selection with Field Parameters
- Slicers and cross-filtering between visuals
- Reset Filters button
- Trend, category-level, and outlet-level analysis
- Consistent Blinkit-inspired visual theme

## Tools & Technologies

| Tool | Usage |
|---|---|
| Power BI Desktop | Dashboard development and visualization |
| Power Query | Data cleaning and transformation |
| DAX | KPI and analytical calculations |
| Excel | Source data |

**Skills applied:** Data Cleaning | Data Modeling | DAX | Interactive Dashboards | Field Parameters | Data Storytelling

## Project Structure

```
blinkit-data-analysis/
├── README.md
├── Power-BI/
│   ├── Blinkit-Sales-Analysis.pbix
│   └── dashboard.png
└── Dataset/
    └── blinkit-data.xlsx
```

## Author

**Sathwik Bhat**
Data Analytics | Power BI | SQL | Python
[LinkedIn](https://www.linkedin.com/in/sathwikbhat/) · [GitHub](https://github.com/sathwikbhat7)
