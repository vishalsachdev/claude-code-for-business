# Exercise 4: Build a Weekly Report Generator

**Time:** 25-30 minutes
**Difficulty:** Intermediate
**You'll build:** A reusable automation that generates weekly reports from raw data

---

## The Business Problem

Every Monday, you generate the same report: summarize last week's key metrics, compare to the week before, highlight wins and concerns. It takes an hour of copy-paste and formatting. Let's turn it into a one-click automation.

---

## What You'll Learn

- What a "script" actually is (demystified)
- Creating reusable automations
- Parameterizing your tools (different dates, files, etc.)
- Scheduling concepts (running automatically)

---

## The Concept: Scripts Aren't Scary

A **script** is just a set of instructions saved to a file. Instead of typing commands one by one, you save them and run them all at once.

Think of it like a recipe:
- **Interactive cooking:** "Chop onions... now add garlic... now..."
- **Recipe:** Follow steps 1-10 in order

Scripts let you "cook" the same report every week without remembering the steps.

---

## The Exercise

### Step 1: Start Claude Code

```bash
cd exercises/04-automation
claude
```

### Step 2: Create Sample Data

First, let's create some weekly metrics data:

```
Create a sample file called weekly_metrics.csv with 8 weeks of business data.
Include: week_ending_date, revenue, new_customers, churn_rate, support_tickets, nps_score
Make the numbers realistic with some variation week to week.
```

### Step 3: Build the Report Interactively

First, do it manually:

```
Analyze weekly_metrics.csv. For the most recent week:
- Show all key metrics
- Compare to the previous week (show % change)
- Identify the biggest win (best improving metric)
- Identify the biggest concern (worst declining metric)
Format as a clean summary.
```

### Step 4: Turn It Into a Script

Now automate it:

```
Turn this analysis into a Python script called generate_weekly_report.py.
The script should:
1. Read the CSV file
2. Analyze the most recent complete week
3. Compare to the previous week
4. Output a formatted report
5. Save the report as weekly_report_[date].md
```

### Step 5: Make It Reusable

Add parameters:

```
Update the script so I can:
- Specify which week to analyze (not just the most recent)
- Choose the output format (markdown or plain text)
- Optionally email the report (just print what would be sent for now)
```

### Step 6: Test Your Automation

Run it:

```
Run the script for the most recent week and show me the output.
```

---

## Expected Output

Your generated report should look like:

```markdown
# Weekly Business Report
**Week Ending: March 17, 2024**
*Generated: March 18, 2024*

## Key Metrics

| Metric | This Week | Last Week | Change |
|--------|-----------|-----------|--------|
| Revenue | $124,500 | $118,200 | +5.3% |
| New Customers | 47 | 52 | -9.6% |
| Churn Rate | 2.1% | 2.4% | -12.5% |
| Support Tickets | 89 | 102 | -12.7% |
| NPS Score | 72 | 68 | +5.9% |

## Highlights

🎉 **Biggest Win:** Support Tickets down 12.7% - team efficiency improving

⚠️ **Concern:** New Customers down 9.6% - may need marketing attention

## Summary

Overall positive week with revenue up and operational metrics improving.
Customer acquisition softness should be monitored.
```

---

## Understanding the Script

Your script will have these basic parts:

```python
# 1. Read the data
data = read_csv("weekly_metrics.csv")

# 2. Get the weeks we need
this_week = get_most_recent_week(data)
last_week = get_previous_week(data)

# 3. Calculate changes
changes = calculate_percent_changes(this_week, last_week)

# 4. Generate the report
report = format_report(this_week, changes)

# 5. Save it
save_report(report, filename)
```

You don't need to understand every line — just the structure. Claude handles the details.

---

## Stretch Goals

1. **Add trends:** Include a 4-week trend for each metric
2. **Conditional alerts:** Flag any metric that changed more than 20%
3. **Historical comparison:** Compare to the same week last month
4. **Multiple formats:** Generate both markdown and HTML versions

---

## Key Concepts

### Why Automation Matters
- **Consistency:** Same format every time
- **Speed:** Seconds instead of an hour
- **Accuracy:** No copy-paste errors
- **Scalability:** Run for different teams, time periods, etc.

### When to Automate
- You do it more than twice
- It's the same steps each time
- Mistakes would be costly
- You could spend the time better elsewhere

---

## Solution Reference

Check the [solution folder](./solution/) for the complete script and sample output.
