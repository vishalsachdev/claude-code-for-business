# Video 1: Your First AI-Built Tool in 30 Minutes

**Target Length:** 35-45 minutes
**Exercise:** Expense Categorizer

---

## Video Structure

| Section | Length | Type |
|---------|--------|------|
| Hook | 0:30 | Face cam |
| Intro | 3:00 | Face cam |
| Installation | 5:00 | Screen + PIP |
| Demo | 20:00 | Screen + PIP |
| Wrap-up | 3:00 | Face cam |

---

## Script Outline

### HOOK (0:00-0:30) — Face Cam

**Goal:** Capture attention, show the outcome

```
"Watch this. I have 100 business expenses in a spreadsheet.
In the next 60 seconds, I'm going to build a tool that categorizes
all of them, calculates totals, and creates a summary report.

[Quick screen cut: run the tool, show output]

No coding required. Just a conversation.

I'm [Name], and in this video, you're going to build the same thing."
```

---

### INTRO (0:30-3:30) — Face Cam

**Goal:** Set expectations, establish credibility, preview the course

**Points to cover:**
- Who this course is for (business students, no coding experience)
- What Claude Code is (AI that builds tools through conversation)
- Why this matters (business people building their own solutions)
- What you'll learn today (install + build your first tool)

```
"If you've ever wished you could just tell a computer what you want
and have it build it for you — that's now possible.

Claude Code is an AI tool that lets you build software through
conversation. No coding experience required. You describe what you
want in plain English, and Claude builds it.

By the end of this video, you'll have:
1. Claude Code installed on your computer
2. Built your first working tool
3. A mental model for how to build more

Let's start by getting Claude Code installed."
```

---

### INSTALLATION (3:30-8:30) — Screen Recording + PIP

**Goal:** Get viewers set up successfully

**Mac Installation:**
```
"I'm going to show Mac first, then Windows.

[Open Terminal]

On Mac, we'll use Homebrew. If you don't have it, pause and
install it from brew.sh first.

Type: brew install claude-code

[Show installation running]

That's it. Now let's verify it works. Type: claude

[Show Claude Code starting up]

You'll need an API key from Anthropic. Go to console.anthropic.com,
create an account, and generate an API key. Paste it when prompted.

[Show the process]
```

**Windows Installation:**
```
"For Windows users...

[Show PowerShell]

Type: winget install Anthropic.ClaudeCode

[Similar process...]
```

**Common issues to address:**
- "Command not found" — close and reopen terminal
- "Invalid API key" — make sure to copy the whole key
- Link to troubleshooting guide for other issues

---

### DEMO (8:30-28:30) — Screen Recording + PIP

**Goal:** Build the expense categorizer step-by-step

#### Phase 1: Explore the Data (3 min)

```
"Now let's build something. I've got this CSV of business expenses.

[Show the CSV file]

100 transactions — dates, descriptions, amounts, vendors.
My accountant wants these categorized with totals.

Let's start by understanding what we're working with."

[In Claude Code]
> Show me what's in expenses.csv. What does the data look like?

[Claude reads and summarizes]

"Notice how Claude just read the file and told us what's in it.
We didn't have to write any code to do that."
```

#### Phase 2: First Attempt (5 min)

```
"Now let's ask for what we actually want."

> Categorize these expenses into groups like Travel, Software,
  Meals, Office Supplies. Show me totals by category.

[Watch Claude work]

"Look at that. Claude analyzed all 100 expenses, figured out
categories based on the descriptions, and gave us totals.

But — let's make it better."
```

#### Phase 3: Iteration (5 min)

```
"This is where the magic happens. We iterate."

> Can you also show percentages of total spending?

[Claude updates]

> Break down Travel into subcategories: Flights, Hotels, Ground Transport

[Claude updates]

"See the pattern? Start with something, then refine it.
You don't need to get it perfect the first time."
```

#### Phase 4: Save and Reuse (5 min)

```
"Now let's make this reusable. Next month, I'll have new expenses.
I don't want to type all this again."

> Turn this into a Python script I can run on any expense CSV.
  Save it as expense_categorizer.py

[Watch Claude create the script]

> Run the script and show me the output

[Demonstrate it works]

"Now I have a tool I can use forever.
New month, new file, same categorization."
```

#### Phase 5: Polish (2 min)

```
"One more thing — let's make the output nicer."

> Format the output as a professional summary I could send to my accountant.
  Save it as expense_report.md

[Claude generates formatted report]

"And now I have a complete expense analysis system."
```

---

### WRAP-UP (28:30-31:30) — Face Cam

**Goal:** Reinforce learning, preview next video, call to action

```
"Let's recap what just happened.

We took a messy CSV of expenses and — through conversation —
built a tool that:
- Reads the data
- Categorizes every transaction
- Calculates totals and percentages
- Generates a formatted report

We didn't write a single line of code ourselves.
We described what we wanted, and Claude built it.

This is the new paradigm: conversation as programming.

In the next video, we'll go deeper into HOW to communicate
effectively with Claude — the patterns that work, the mistakes
to avoid, and how to get exactly what you want.

Your homework: Go to the exercise folder and try building the
expense categorizer yourself. The starter files are there.

I'm [Name]. Thanks for watching. See you in Video 2."
```

---

## B-Roll / Visual Notes

### Screen recording tips:
- Increase terminal font size for readability
- Clean desktop — hide distractions
- Type slowly enough for viewers to follow
- Pause briefly when something important appears

### Face cam segments:
- Good lighting
- Clean background
- Maintain energy — this is the hook video

### Cuts to add:
- Quick cut showing the final output early (the hook)
- Split screen showing before/after (CSV vs report)
- Zoom on key parts of output

---

## Timestamps for YouTube Description

```
0:00 - Hook
0:30 - What is Claude Code?
3:30 - Installation (Mac)
5:30 - Installation (Windows)
7:00 - API Key Setup
8:30 - Demo Start: Exploring the Data
11:30 - Building the Categorizer
16:30 - Iterating and Refining
21:30 - Saving as Reusable Script
26:30 - Generating Professional Report
28:30 - Wrap-up & Next Steps
```

---

## Notes for Recording

- Energy level: High but not manic — excited, confident, helpful
- Pace: Slightly slower than natural speech for comprehension
- Mistakes: Leave in some genuine moments of iteration (not scripted errors)
- Tone: Teacher who's excited about what they're sharing

---

## Thumbnail Concepts

1. Split image: Messy spreadsheet → Clean report, with "30 MINUTES" text
2. Terminal with Claude Code + surprised/excited face
3. Before/After: "100 expenses → 1 click"
