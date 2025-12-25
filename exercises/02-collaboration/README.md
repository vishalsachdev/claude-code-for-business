# Exercise 2: Transform a Business Memo

**Time:** 20-25 minutes
**Difficulty:** Beginner
**You'll build:** A structured analysis from an unstructured memo

---

## The Business Problem

Your manager forwarded you a long, rambling memo from a client meeting. You need to extract the action items, key decisions, stakeholders, and timeline. Instead of reading it three times and making notes, let's do it in one pass.

---

## What You'll Learn

- How to give Claude context about your goal
- How to specify output format
- The art of iteration: start broad, then refine
- How to handle ambiguous requests

---

## The Starting Material

Create a file called `client_memo.txt` in this folder with the following content (or copy from below):

```
From: Sarah Johnson
Date: March 15, 2024
Subject: Notes from Acme Corp meeting

Met with Acme today. Bob (their CTO) was there along with Lisa from procurement
and someone from legal whose name I didn't catch.

They're interested in our Enterprise plan but have concerns about the
implementation timeline. Originally wanted to go live by Q2 but that seems
aggressive given their legacy system situation. I suggested Q3 might be more
realistic and they seemed okay with that.

Bob mentioned they'd need SSO integration - apparently that's non-negotiable
for their security team. Also wants API access for their internal dashboards.
Lisa said budget is approved for up to $50k annually but would need to go
back to finance if we're over that.

They're currently using WidgetCorp (our competitor) but unhappy with support
response times. This is a real opportunity.

Action items from my side:
- Send them the enterprise pricing sheet
- Schedule a technical deep-dive with their IT team
- Get timeline from implementation team

Need to follow up within a week - Bob is presenting to their board on the 25th
and wants our info before then.

Oh also they asked about training - how many hours included? I said I'd check.
And data migration - they have 5 years of historical data they want to bring over.

Good meeting overall. Think we have a real shot at this one.
```

---

## The Exercise

### Step 1: Start Claude Code in This Folder

```bash
cd exercises/02-collaboration
claude
```

### Step 2: First Attempt - Be Vague on Purpose

Try a vague request first to see what happens:

```
Analyze the client memo in client_memo.txt
```

Notice: Claude will give you *something*, but it might not be what you need. This is the starting point.

### Step 3: Add Context About Your Goal

Now be specific about what you're trying to accomplish:

```
I need to send my manager a structured summary of this client meeting memo.
Extract: key stakeholders, their concerns, budget info, timeline, and action items.
Format it as something I can paste into an email.
```

See how the output changes when Claude knows the purpose?

### Step 4: Specify the Exact Format

Get even more specific:

```
Format this as:
1. STAKEHOLDERS (name, role, key concerns)
2. DEAL SUMMARY (one paragraph)
3. BUDGET & TIMELINE (bullet points)
4. ACTION ITEMS (with deadlines)
5. RISKS/CONCERNS (what could go wrong)
```

### Step 5: Iterate on Specific Sections

Maybe the action items need work:

```
For the action items, add suggested owners and priority levels.
Also, calculate the actual deadline date based on "within a week" from the memo date.
```

---

## Expected Output

Your final summary should look something like:

```
## STAKEHOLDERS
- **Bob** (CTO) - Key decision maker. Concerns: SSO integration, API access, implementation timeline
- **Lisa** (Procurement) - Budget holder. Approved up to $50k/year
- **[Unknown]** (Legal) - Present but role unclear

## DEAL SUMMARY
Acme Corp is considering our Enterprise plan as a replacement for WidgetCorp...

## BUDGET & TIMELINE
- Budget: Up to $50k annually (approved)
- Original target: Q2 2024
- Revised target: Q3 2024 (recommended by us, accepted)
- Critical date: March 25, 2024 (Bob's board presentation)

## ACTION ITEMS
| Action | Owner | Priority | Deadline |
|--------|-------|----------|----------|
| Send enterprise pricing sheet | Me | High | Mar 18 |
| Schedule technical deep-dive | Me | High | Mar 20 |
| Get implementation timeline | Implementation Team | High | Mar 20 |
| Clarify training hours | Me | Medium | Mar 20 |
| Assess data migration scope | Technical Team | Medium | Mar 22 |

## RISKS/CONCERNS
- SSO is non-negotiable - must confirm we support their requirements
- 5 years of data migration could be complex
- Tight timeline before board presentation
```

---

## Key Patterns Learned

### 1. Context First
"I need this for [purpose]" changes everything.

### 2. Format Explicitly
Don't say "summarize" — say "format as X with sections Y and Z"

### 3. Iterate, Don't Start Over
"Also add X" is better than re-explaining everything

### 4. Ask for Inference
Claude can calculate deadlines, identify risks, suggest priorities

---

## Stretch Goal

1. **Create a template:** Turn this into a reusable prompt for future meeting memos
2. **Generate follow-up email:** Ask Claude to draft the email to Bob
3. **Competitor comparison:** Add a section comparing mentioned competitor weaknesses to your strengths

---

## Solution Reference

Check the [solution folder](./solution/) for the expected analysis format.
