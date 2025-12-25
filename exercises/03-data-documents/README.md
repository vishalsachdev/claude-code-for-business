# Exercise 3: Build a Sales Data Analyzer

**Time:** 25-30 minutes
**Difficulty:** Intermediate
**You'll build:** An automated sales analysis tool with insights and visualizations

---

## The Business Problem

Your company has quarterly sales data. Leadership wants to know: What's selling? Where? Who are the top performers? What trends should we watch? Currently, someone spends 4 hours in Excel doing this manually. Let's automate it.

---

## What You'll Learn

- Working with larger datasets (100+ rows)
- Asking for specific analyses (grouping, aggregation, trends)
- Creating data visualizations
- Generating executive-ready reports

---

## The Data

You have `sales_data.csv` with columns:
- `date` - When the sale occurred
- `product` - Widget Basic, Widget Pro, or Widget Enterprise
- `region` - Northeast, Southeast, Midwest, West
- `units_sold` - Number of units
- `revenue` - Dollar amount
- `cost` - Cost of goods sold
- `salesperson` - Who made the sale

---

## The Exercise

### Step 1: Start Claude Code

```bash
cd exercises/03-data-documents
claude
```

### Step 2: Understand the Data

First, get oriented:

```
Look at sales_data.csv. How many rows? What's the date range?
Show me a summary of the data structure.
```

### Step 3: Basic Aggregations

Start with the fundamentals:

```
Create a sales summary showing:
- Total revenue by product
- Total revenue by region
- Top 5 days by revenue
```

### Step 4: Deeper Analysis

Now ask smarter questions:

```
Calculate profit margin by product (revenue - cost / revenue).
Which product has the best margin? Which region is most profitable?
```

### Step 5: Trend Analysis

Look at time patterns:

```
Show me weekly revenue trends. Is sales growing or declining?
Are there any notable patterns by day of week?
```

### Step 6: Salesperson Performance

```
Rank salespeople by:
1. Total revenue
2. Number of deals
3. Average deal size
4. Most improved (comparing first half to second half of data)
```

### Step 7: Generate an Executive Summary

Pull it all together:

```
Create an executive summary report as a markdown document. Include:
- Key metrics (total revenue, units, profit)
- Top performers (products, regions, people)
- Trends and insights
- Recommended actions

Save it as sales_report.md
```

---

## Expected Insights

Your analysis should reveal things like:

- **Product mix:** Enterprise has highest margin but lowest volume
- **Regional performance:** Northeast leads in revenue but West is growing fastest
- **Salesperson insights:** Sarah Chen dominates Enterprise sales; David Kim has the highest volume
- **Trends:** Revenue grew 15% from January to March

---

## Stretch Goals

1. **Visualization:** Ask Claude to create a simple chart (bar chart of revenue by region)
2. **Forecasting:** "Based on trends, project next month's revenue"
3. **Anomaly detection:** "Flag any unusual sales patterns or outliers"
4. **Comparison script:** Create a reusable script that compares any two months

---

## Key Techniques

### Asking Good Data Questions
- "Group by X and show Y" → aggregation
- "Compare A to B" → differential analysis
- "Is there a pattern in..." → trend detection
- "What's unusual about..." → anomaly detection

### Getting Reusable Output
- "Save this as a script"
- "Create a function I can run with different dates"
- "Make this into a report template"

---

## Solution Reference

Check the [solution folder](./solution/) for sample analysis output and the executive report template.
