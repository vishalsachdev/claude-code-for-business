# Exercise 5: Build a Competitor Analysis Tool

**Time:** 30-35 minutes
**Difficulty:** Intermediate
**You'll build:** An automated competitive intelligence analyzer

---

## The Business Problem

You're preparing for a strategy meeting and need to understand your competitive landscape. You have some data on competitors, but analyzing it manually is tedious. Let's build a tool that creates actionable competitive intelligence.

---

## What You'll Learn

- Working with JSON data (structured information)
- Asking comparative questions
- Generating strategic insights
- Creating research templates

---

## The Data

You have `competitors.json` containing:
- Competitor company profiles
- Product offerings and pricing
- Strengths and weaknesses
- Recent news and developments
- Market summary data

---

## The Exercise

### Step 1: Start Claude Code

```bash
cd exercises/05-market-research
claude
```

### Step 2: Explore the Competitive Data

```
Read competitors.json. Give me a quick overview:
- How many competitors are tracked?
- What information do we have on each?
```

### Step 3: Pricing Comparison

```
Create a pricing comparison table. Show each competitor's products,
prices, and what's included at each tier. Make it easy to see where
we might have an advantage or disadvantage.
```

### Step 4: SWOT-Style Analysis

```
For each competitor, create a quick competitive assessment:
- Their biggest strength (what they do better than us)
- Their biggest weakness (our opportunity)
- Threat level (High/Medium/Low) with reasoning
```

### Step 5: Identify Market Opportunities

```
Based on the market summary and competitor weaknesses, identify:
- 3 market opportunities we should pursue
- Which competitor is most vulnerable to our strengths
- What features/capabilities would help us win more deals
```

### Step 6: Generate a Battle Card

```
Create a "battle card" for our sales team to use against WidgetCorp
(our main competitor). Include:
- Key differentiators
- Common objections and responses
- Pricing positioning
- Recent news they should know
Format it as something salespeople can reference in 30 seconds.
```

### Step 7: Save as a Reusable Template

```
Save the competitive analysis as competitive_analysis.md.
Also create a template I can use when adding new competitors to track.
```

---

## Expected Outputs

### Pricing Comparison Table

| Company | Entry Price | Mid-tier | Enterprise |
|---------|-------------|----------|------------|
| WidgetCorp | $49 | $99 | Custom |
| SimpleWidgets | Free | $29 | $79 |
| MegaWidget | $149 | $299 | $500+ |
| WidgetFlow | $19 | $49 | - |

### Battle Card Example

```
# BATTLE CARD: vs WidgetCorp

## Quick Stats
- Founded: 2015 | Employees: 50-100 | Funding: $12M Series A

## Why Customers Choose Us Over Them
✓ Simpler onboarding (they're complex)
✓ Better pricing for SMBs
✓ Faster support response times (their weakness!)

## Common Objections
"WidgetCorp has more integrations"
→ Response: "We cover the top 10 integrations that matter. Which ones do you need?"

"WidgetCorp is more established"
→ Response: "We're established enough to be trusted but nimble enough to innovate fast."

## Pricing Positioning
- Their Basic ($49) vs Our Pro ($XX) - highlight value difference
- Watch for: They discount aggressively at end of quarter

## Recent Intel
- Acquired DataSync (Feb 2024) - may have integration disruptions
- Launched mobile app - still buggy based on reviews
```

---

## Stretch Goals

1. **Competitive monitoring script:** Create a template for tracking competitor updates monthly
2. **Feature comparison matrix:** Detailed feature-by-feature comparison
3. **Win/loss analysis template:** Create a structure for tracking why you win or lose against each competitor
4. **Quarterly competitive report:** Template for regular competitive updates to leadership

---

## Key Research Patterns

### Good Competitive Questions
- "How do they position against us?"
- "Where are they weak that we're strong?"
- "What would make a customer choose them over us?"
- "What's changed recently?"

### Turning Data Into Action
- Raw data → Analysis → Insights → Actions
- "They raised prices" → "Opportunity to win price-sensitive customers"
- "They launched mobile app" → "We should accelerate our mobile roadmap"

---

## Solution Reference

Check the [solution folder](./solution/) for sample analysis and battle card templates.
