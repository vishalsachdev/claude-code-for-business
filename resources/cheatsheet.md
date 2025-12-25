# Claude Code Cheatsheet

Quick reference for common commands and patterns.

---

## Starting Claude Code

```bash
# Start Claude Code in current directory
claude

# Start with a specific task in mind
claude "analyze the sales data in this folder"
```

---

## Essential Commands

| Command | What It Does |
|---------|--------------|
| `claude` | Start a new conversation |
| `Ctrl+C` | Cancel current operation |
| `Ctrl+D` | Exit Claude Code |
| `/help` | Show available commands |
| `/clear` | Clear conversation history |

---

## Effective Prompting Patterns

### 1. Start with the Goal
**Instead of:** "Read the CSV file"
**Say:** "I have a CSV of expenses. Categorize each transaction and create a summary by category."

### 2. Provide Context
**Instead of:** "Fix the errors"
**Say:** "This sales report has missing values in the region column. Fill them based on the city names."

### 3. Specify Output Format
**Instead of:** "Summarize this data"
**Say:** "Summarize this data as a markdown table with columns: Category, Total, Count"

### 4. Iterate and Refine
- Start broad, then narrow down
- "That's close, but can you also add percentages?"
- "Good. Now make it only show the top 5 categories."

---

## Working with Files

### Reading Files
```
"Read the expenses.csv file and show me the first 10 rows"
"What columns are in sales_data.csv?"
"Summarize the contents of this folder"
```

### Creating Files
```
"Create a Python script that categorizes expenses"
"Generate a report and save it as report.md"
"Export the results to a new CSV called output.csv"
```

### Editing Files
```
"Update the script to also calculate averages"
"Add error handling to the categorizer"
"Change the output format to include dates"
```

---

## Common Tasks

### Data Analysis
```
"Analyze this CSV and tell me the key insights"
"What's the total by category?"
"Show me trends over time"
"Find any outliers or anomalies"
```

### Automation
```
"Create a script I can run weekly to generate this report"
"Make this process repeatable"
"Add the ability to process multiple files"
```

### Building Tools
```
"Build a simple web interface for this"
"Create a dashboard showing these metrics"
"Make this interactive so users can filter by date"
```

---

## Troubleshooting

### "Claude doesn't understand what I want"
- Be more specific about the desired output
- Provide an example of what you're looking for
- Break the task into smaller steps

### "The code has errors"
- Tell Claude: "This gives an error when I run it. Can you fix it?"
- Share the error message if you see one

### "It's doing something different than I expected"
- Clarify: "I meant X, not Y"
- Provide a concrete example of what you want

### "I want to undo changes"
- Say: "Revert to the previous version"
- Use git if you have it set up: `git checkout filename`

---

## Best Practices

1. **Start small** — Get one thing working before adding complexity
2. **Save frequently** — Ask Claude to save working versions
3. **Test as you go** — Try the tool after each change
4. **Name things clearly** — "expense_categorizer.py" not "script.py"
5. **Keep context** — Claude remembers your conversation, refer to previous work

---

## Example Conversation Flow

```
You: I have a CSV of business expenses. Can you help me categorize them?

Claude: I'd be happy to help! Let me first look at your CSV to understand
the structure. [reads file] I see columns for date, description, amount.
Do you want me to create categories based on the descriptions?

You: Yes, and group them by category with totals.

Claude: [creates categorizer] Done! I've created categories like
"Office Supplies", "Travel", "Software". The total by category is...

You: Perfect. Can you also show the percentage of total spending?

Claude: [updates output] Here's the updated summary with percentages...

You: Great. Save this as a script I can run again next month.

Claude: [creates reusable script] Created expense_categorizer.py.
Just run it with: python expense_categorizer.py your_file.csv
```

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `↑` | Previous message |
| `↓` | Next message |
| `Ctrl+C` | Cancel |
| `Ctrl+D` | Exit |
| `Tab` | Autocomplete file names |

---

*Keep this open in another tab while you work!*
