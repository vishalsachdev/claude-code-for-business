# Troubleshooting Guide

Common issues and how to fix them.

---

## Installation Issues

### "Command not found: claude"

**Mac:**
```bash
# Make sure Homebrew is installed first
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Then install Claude Code
brew install claude-code
```

**Windows:**
```powershell
# Make sure winget is available (Windows 10/11)
winget install Anthropic.ClaudeCode
```

**Still not working?**
- Close and reopen your terminal
- Try running with the full path

---

### "Invalid API key"

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Navigate to API Keys
3. Create a new key (or copy existing one)
4. Run `claude` and paste the key when prompted

**Note:** Keys start with `sk-ant-`. Make sure you copied the full key.

---

### "Rate limit exceeded" or "Insufficient credits"

- Free tier has usage limits
- Add billing at console.anthropic.com to increase limits
- Wait a few minutes and try again for temporary limits

---

## Common Errors

### "File not found"

Claude Code works in your current directory. Make sure you're in the right folder:

```bash
# Check where you are
pwd

# Move to the exercise folder
cd exercises/01-first-contact

# List files to confirm
ls
```

---

### "Permission denied"

**Mac/Linux:**
```bash
# Make the script executable
chmod +x your_script.py
```

**Windows:**
- Right-click the file → Properties → Unblock

---

### Code runs but produces wrong output

1. **Check the input:** "Can you show me the first few rows of the file you're reading?"
2. **Verify understanding:** "What columns do you see in this data?"
3. **Be more specific:** "I want X grouped by Y, showing Z"

---

### "I can't see what Claude is doing"

Ask Claude to show its work:
- "Show me the code before running it"
- "Explain what this script does step by step"
- "Print intermediate results so I can see what's happening"

---

## Getting Unstuck

### Claude misunderstood me

Be direct:
- "That's not what I meant. I want..."
- "Stop. Let me clarify..."
- "Ignore that last request. Instead..."

### The solution is too complex

Ask for simplicity:
- "Can you make this simpler?"
- "Just do the minimum to solve this"
- "I don't need [feature], remove it"

### I don't understand what Claude built

Ask for explanation:
- "Walk me through this code line by line"
- "What does this part do?"
- "Explain this like I've never coded before"

### I broke something

- "Undo the last change"
- "Revert to the version that was working"
- Check the solution folder for reference

---

## Exercise-Specific Issues

### Exercise 1: Expense Categorizer
- Make sure `expenses.csv` is in the current folder
- Check that the CSV has headers (date, description, amount)

### Exercise 3: Sales Analyzer
- Large files may take a moment to process
- If it's slow, ask to analyze a sample first

### Exercise 7: Dashboard
- You need a web browser to view the result
- Claude will tell you what URL to open (usually localhost:3000)

---

## When to Start Fresh

Sometimes it's easier to start over:

```bash
# Clear the conversation
/clear

# Or exit and restart
Ctrl+D
claude
```

This gives you a fresh start without accumulated context.

---

## Getting Help

### In Claude Code
- Ask: "I'm stuck on X, can you help?"
- Claude can often diagnose issues if you describe what's happening

### Course Resources
- Check the solution folder in each exercise
- Review the video for that section

### External Resources
- [Claude Code Documentation](https://docs.anthropic.com/claude-code)
- [Anthropic Discord](https://discord.gg/anthropic)

---

## Pro Tips

1. **Read error messages** — They often tell you exactly what's wrong
2. **Try the simplest thing** — Before complex solutions, try the obvious fix
3. **Save working versions** — Before making big changes, save what works
4. **Ask Claude to debug** — "This error appeared: [paste error]. What's wrong?"

---

*Most problems have simple solutions. When in doubt, ask Claude!*
