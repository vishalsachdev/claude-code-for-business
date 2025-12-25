# Exercise 1: Build an Expense Categorizer

**Time:** 15-20 minutes
**Difficulty:** Beginner
**You'll build:** A tool that automatically categorizes business expenses

---

## The Business Problem

You have a CSV of business expenses. Your accountant wants them categorized (Travel, Software, Meals, Office Supplies, etc.) with totals by category. Doing this manually takes hours. Let's automate it.

---

## What You'll Learn

- How to start Claude Code and navigate the terminal
- How to describe what you want in plain English
- How to read files and create output
- The basics of iterating on your request

---

## Before You Start

Make sure you have:
- [ ] Claude Code installed (`claude` command works in your terminal)
- [ ] This folder open in your terminal

To get to this folder:
```bash
cd path/to/claude-code-for-business/exercises/01-first-contact
```

---

## The Exercise

### Step 1: Start Claude Code

Open your terminal and navigate to this folder, then type:

```bash
claude
```

You should see Claude Code start up and wait for your input.

### Step 2: Explore the Data

Before building anything, look at what you're working with. Try:

```
What's in the expenses.csv file? Show me the first few rows.
```

Notice how Claude reads the file and shows you the structure. You'll see columns for date, description, amount, and vendor.

### Step 3: Request the Categorization

Now describe what you want:

```
Categorize these expenses into groups like Travel, Software, Meals & Entertainment,
Office Supplies, Marketing, etc. Create a summary showing totals by category.
```

Watch as Claude:
1. Reads all the expenses
2. Analyzes the descriptions
3. Assigns categories
4. Creates a summary

### Step 4: Refine the Output

Maybe you want more detail. Try:

```
Can you also show the percentage of total spending for each category?
```

Or:

```
Break down Travel into subcategories: Flights, Hotels, Ground Transportation.
```

### Step 5: Save Your Work

When you're happy with the result:

```
Save this as a Python script I can run again with new expense files.
```

---

## Expected Output

Your categorization should look something like this:

```
Expense Summary by Category
===========================

Travel                  $8,234.50  (32%)
├── Flights             $4,729.00
├── Hotels              $3,144.00
├── Ground Transport    $361.50

Software & Subscriptions $1,245.67  (5%)
├── Zoom                $59.96
├── AWS                 $543.43
├── Other subscriptions $642.28

Meals & Entertainment   $2,456.80  (10%)
├── Client meals        $1,523.40
├── Team meals          $933.40

... (and so on)

Total Expenses: $25,432.15
```

---

## Stretch Goal

If you finish early, try these challenges:

1. **Add vendor analysis:** Which vendors do you spend the most with?
2. **Monthly breakdown:** Show expenses by month AND category
3. **Flag unusual expenses:** Have Claude identify any outliers

---

## Common Issues

**"Claude can't find the file"**
- Make sure you're in the right folder (use `pwd` to check)
- File is `expenses.csv` (check with `ls`)

**"Categories don't make sense"**
- Be more specific: "Use these exact categories: Travel, Software, Meals, Office, Marketing, Professional Services"

**"I want different output"**
- Just ask! "Format this as a markdown table" or "Show it as a bulleted list"

---

## What You Built

You just created a working expense categorizer! The key insight: you described a business problem in plain English, and Claude turned it into a working solution.

This same pattern works for thousands of business tasks:
- Describe what you want
- Let Claude show you a first attempt
- Refine until it's right
- Save for reuse

---

## Next Up

In [Exercise 2](../02-collaboration/), you'll learn the patterns for communicating effectively with Claude — how to give context, set constraints, and iterate productively.

---

## Solution Reference

If you get stuck, check the [solution folder](./solution/) for reference code and expected output.
