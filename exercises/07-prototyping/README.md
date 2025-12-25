# Exercise 7: Build a Customer Feedback Dashboard

**Time:** 35-45 minutes
**Difficulty:** Advanced
**You'll build:** An interactive web dashboard displaying customer feedback insights

---

## The Business Problem

Your customer success team collects feedback constantly, but insights are buried in spreadsheets. Leadership wants a dashboard they can check anytime to see: How happy are customers? What are they asking for? What needs attention? Let's build it.

---

## What You'll Learn

- Building simple web interfaces
- Creating interactive data visualizations
- The MVP (Minimum Viable Product) mindset
- When to ship vs. when to polish

---

## The Data

You have `customer_feedback.csv` with:
- 30 customer feedback entries
- Ratings, NPS scores, categories
- Feedback text and sentiment
- Resolution status

---

## The MVP Mindset

Before we build, an important concept:

**MVP = Minimum Viable Product**

Build the smallest thing that provides value. Then iterate.

❌ Don't: Try to build Salesforce in an afternoon
✅ Do: Build a dashboard that answers 3 key questions well

Our 3 questions:
1. **Overall health:** What's our average rating/NPS?
2. **What's broken:** What negative feedback needs attention?
3. **What's wanted:** What features are customers requesting?

---

## The Exercise

### Step 1: Start Claude Code

```bash
cd exercises/07-prototyping
claude
```

### Step 2: Understand the Feedback Data

```
Analyze customer_feedback.csv. Give me:
- Total number of feedback entries
- Distribution of ratings (1-5)
- Distribution by category
- Sentiment breakdown
```

### Step 3: Build the Dashboard - Version 1

Start simple:

```
Create a simple HTML dashboard that shows:
- Average rating (big number, prominent)
- NPS score (big number, color coded: green if 50+, yellow 30-50, red below 30)
- Count of unresolved issues
- List of negative feedback items (rating 1-2) that aren't resolved

Save it as dashboard.html. Make it clean and simple.
```

### Step 4: Open and Review

```
How do I open this dashboard in my browser?
```

(Claude will tell you to open the HTML file directly or run a simple server)

### Step 5: Add Interactivity

```
Enhance the dashboard:
- Add a filter to show feedback by category
- Make the negative feedback items clickable to see full details
- Add a "Most Requested Features" section based on feature_request category
```

### Step 6: Add Basic Visualization

```
Add a simple bar chart showing feedback volume by category.
Use a simple JavaScript charting library or pure CSS bars.
Keep it clean — no complex setup.
```

### Step 7: Make It Refresh-Ready

```
Update the dashboard so it can easily be refreshed with new data.
Create a separate data.js file that the HTML reads from, so I can
update the data without touching the HTML structure.
```

---

## Expected Output

Your dashboard should show:

```
┌─────────────────────────────────────────────────────┐
│  CUSTOMER FEEDBACK DASHBOARD                        │
├─────────────────────────────────────────────────────┤
│                                                     │
│  ⭐ 3.8        📊 72 NPS        ⚠️ 5 Unresolved    │
│  Avg Rating    (Good)          Issues              │
│                                                     │
├─────────────────────────────────────────────────────┤
│  NEEDS ATTENTION                                    │
│  • Dashboard crashes on export - Amanda Foster      │
│  • Data sync failing - James Wilson                 │
│  • Pages load slowly - Karen Davis                  │
│  [View all 5 unresolved →]                         │
│                                                     │
├─────────────────────────────────────────────────────┤
│  TOP FEATURE REQUESTS                               │
│  1. Dark mode (3 requests)                         │
│  2. Slack integration (2 requests)                  │
│  3. Custom fields (2 requests)                      │
│                                                     │
├─────────────────────────────────────────────────────┤
│  FEEDBACK BY CATEGORY                               │
│  [Bar chart visualization]                          │
└─────────────────────────────────────────────────────┘
```

---

## The MVP Process

### What We Built (MVP)
- Key metrics at a glance
- Prioritized issues list
- Feature request tracking
- Basic filtering

### What We Didn't Build (Future Iterations)
- User authentication
- Real-time data connection
- Complex filtering/sorting
- Mobile responsiveness
- Export functionality

**This is intentional.** Ship something useful, get feedback, iterate.

---

## Stretch Goals

1. **Add trends:** Show this week vs. last week comparison
2. **Sentiment analysis:** Use color coding for feedback sentiment
3. **Email alerts:** Generate an HTML email template for weekly digest
4. **Customer details:** Click a customer name to see all their feedback history

---

## Key Prototyping Principles

### 1. Start with Questions, Not Features
"What do users need to know?" > "What features should we build?"

### 2. Ugly and Working > Pretty and Incomplete
A functional prototype beats a beautiful mockup.

### 3. Use Real Data
Fake data hides problems. Real data shows what actually matters.

### 4. Ship and Iterate
Perfect is the enemy of good. Get feedback early.

---

## Solution Reference

Check the [solution folder](./solution/) for the complete dashboard code and styling suggestions.
