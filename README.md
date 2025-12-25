# Claude Code for Business Builders

Build functional business tools using AI — no coding experience required.

## What This Course Is

An 8-video series that takes you from "I've never used a terminal" to "I just built a working business tool." Each video includes hands-on exercises with real datasets you can follow along with.

**By the end, you'll be able to:**
- Turn business problems into working solutions through conversation
- Build tools for data analysis, automation, and prototyping
- Create a portfolio of functional tools you actually built

## Who This Is For

- Business students and MBA candidates
- Entrepreneurs who want to prototype faster
- Analysts who want to automate repetitive work
- Anyone curious about AI-assisted development

**Prerequisites:** Basic computer skills. That's it.

## Course Videos

| # | Video | What You'll Build |
|---|-------|-------------------|
| 1 | [First Contact](#video-1-first-contact) | Expense categorizer |
| 2 | [The Collaboration Paradigm](#video-2-the-collaboration-paradigm) | Business memo analyzer |
| 3 | [Data & Documents](#video-3-data--documents) | Sales data analyzer |
| 4 | [Automation Fundamentals](#video-4-automation-fundamentals) | Weekly report generator |
| 5 | [Market Research Toolkit](#video-5-market-research-toolkit) | Competitor analysis tool |
| 6 | [Content & Marketing](#video-6-content--marketing) | Content repurposing tool |
| 7 | [Prototyping Business Apps](#video-7-prototyping-business-apps) | Customer feedback dashboard |
| 8 | [Capstone Project](#video-8-capstone-project) | Your own custom tool |

---

## Getting Started

### Step 1: Install Claude Code

Choose your operating system and follow the instructions below.

---

<details>
<summary><strong>🍎 Mac Installation (click to expand)</strong></summary>

#### Option A: Using Homebrew (Recommended)

**1. Open Terminal**
- Press `Cmd + Space`, type "Terminal", press Enter
- Or find Terminal in Applications → Utilities

**2. Install Homebrew (if you don't have it)**

Check if you have Homebrew:
```bash
brew --version
```

If you see "command not found", install Homebrew:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Follow the prompts. This may take a few minutes.

**3. Install Claude Code**
```bash
brew install claude-code
```

**4. Verify installation**
```bash
claude --version
```
You should see a version number.

#### Option B: Using npm

If you have Node.js installed:
```bash
npm install -g @anthropic-ai/claude-code
```

#### Troubleshooting Mac

- **"command not found: brew"** — Close Terminal, reopen, try again. If still not working, run the Homebrew install command again.
- **"permission denied"** — Try `sudo brew install claude-code` and enter your password.
- **M1/M2 Mac issues** — Make sure Homebrew is installed for Apple Silicon. Run `which brew` — it should show `/opt/homebrew/bin/brew`.

</details>

---

<details>
<summary><strong>🪟 Windows Installation (click to expand)</strong></summary>

#### Option A: Using winget (Recommended for Windows 10/11)

**1. Open PowerShell as Administrator**
- Press `Windows + X`
- Click "Windows Terminal (Admin)" or "PowerShell (Admin)"
- Click "Yes" if prompted

**2. Check if winget is available**
```powershell
winget --version
```
If you see a version number, proceed. If not, [install App Installer from Microsoft Store](https://apps.microsoft.com/store/detail/app-installer/9NBLGGH4NNS1).

**3. Install Claude Code**
```powershell
winget install Anthropic.ClaudeCode
```

**4. Close and reopen PowerShell, then verify**
```powershell
claude --version
```

#### Option B: Using npm

If you have Node.js installed:
```powershell
npm install -g @anthropic-ai/claude-code
```

#### Option C: Direct Download

1. Go to [Claude Code releases](https://github.com/anthropics/claude-code/releases)
2. Download the Windows installer (.exe)
3. Run the installer and follow prompts
4. Restart your terminal

#### Troubleshooting Windows

- **"winget not recognized"** — You need Windows 10 (1809+) or Windows 11. Update Windows or install from Microsoft Store.
- **"Access denied"** — Make sure you're running PowerShell as Administrator.
- **"claude not recognized" after install** — Close ALL terminal windows and open a new one. The PATH needs to refresh.
- **Antivirus blocking** — Some antivirus software blocks new CLI tools. Add an exception for Claude Code.

</details>

---

### Step 2: Choose How to Access Claude

You have three options. Pick the one that works best for you:

---

<details>
<summary><strong>Option A: Anthropic Account (Easiest)</strong></summary>

Use your Anthropic account directly — no API key needed.

1. **Create an Anthropic account** at [claude.ai](https://claude.ai)
2. **Run Claude Code:**
   ```bash
   claude
   ```
3. **Choose "Login with Anthropic"** when prompted
4. **Follow the browser link** to authenticate

This uses your existing Claude subscription (Pro/Free). See [official docs](https://docs.anthropic.com/en/docs/claude-code/overview) for details.

</details>

---

<details>
<summary><strong>Option B: Anthropic API Key (Pay-as-you-go)</strong></summary>

Use the Anthropic API for more control and usage-based pricing.

1. **Go to** [console.anthropic.com](https://console.anthropic.com)
2. **Create an account** or sign in
3. **Generate an API key:**
   - Click "API Keys" in sidebar
   - Click "Create Key"
   - **Copy immediately** — you won't see it again!
4. **Add billing** (required for API usage)
5. **Run Claude Code:**
   ```bash
   claude
   ```
6. **Paste your API key** when prompted (starts with `sk-ant-`)

See [Anthropic API documentation](https://docs.anthropic.com/en/docs/claude-code/overview) for pricing and limits.

</details>

---

<details>
<summary><strong>Option C: Free via OpenRouter + Claudish (No Cost)</strong></summary>

Use Claude Code for **free** through OpenRouter's free tier models.

**Step 1: Get an OpenRouter API Key**
1. Go to [openrouter.ai](https://openrouter.ai)
2. Create a free account
3. Go to [openrouter.ai/keys](https://openrouter.ai/keys)
4. Create a new API key and copy it

**Step 2: Find the Best Free Model**
1. Go to [openrouter.ai/models](https://openrouter.ai/models)
2. Filter by "Free" in the pricing dropdown
3. Look for capable free models like:
   - `google/gemini-2.0-flash-exp:free`
   - `meta-llama/llama-3.1-8b-instruct:free`
   - `mistralai/mistral-7b-instruct:free`
4. Copy the model ID (e.g., `google/gemini-2.0-flash-exp:free`)

**Step 3: Use Claudish**
1. Go to [claudish.com](https://claudish.com)
2. This is a Claude Code-compatible interface that works with OpenRouter
3. Enter your OpenRouter API key
4. Select your chosen free model
5. Start building!

**Note:** Free models are less capable than Claude, but great for learning the workflow. You can upgrade later.

</details>

---

### Step 3: Verify It's Working

Run Claude Code:
```bash
claude
```

You should see Claude Code start and wait for your input. Type something like:
```
Hello! Can you confirm you're working?
```

If you get a response, you're ready to go!

### Step 4: Clone This Course Repo

**If you have git installed:**
```bash
git clone https://github.com/vishalsachdev/claude-code-for-business.git
cd claude-code-for-business
```

**If you don't have git:**
1. Click the green "Code" button on this GitHub page
2. Click "Download ZIP"
3. Extract the ZIP file
4. Open Terminal/PowerShell and navigate to the extracted folder

### Step 5: Start with Video 1

Navigate to the first exercise:
```bash
cd exercises/01-first-contact
```

Then start Claude Code:
```bash
claude
```

You're ready to build your first tool!

---

## Course Structure

### Video 1: First Contact
**"Your First AI-Built Tool in 30 Minutes"**

Learn what Claude Code is, install it, and build your first working tool — an expense categorizer that reads a CSV and organizes transactions by category.

[Go to Exercise →](exercises/01-first-contact/)

---

### Video 2: The Collaboration Paradigm
**"Thinking Like an AI Collaborator"**

Master the art of describing what you want. Learn iteration, refinement, and how to avoid common beginner mistakes.

[Go to Exercise →](exercises/02-collaboration/)

---

### Video 3: Data & Documents
**"Turn Your Spreadsheets Into Insights"**

Work with CSVs, create reports, and build tools that analyze your business data automatically.

[Go to Exercise →](exercises/03-data-documents/)

---

### Video 4: Automation Fundamentals
**"Make It Repeatable"**

Understand what scripts are (without the jargon) and build automations you can run again and again.

[Go to Exercise →](exercises/04-automation/)

---

### Video 5: Market Research Toolkit
**"AI-Powered Competitive Intelligence"**

Build tools for web research, competitor analysis, and market intelligence gathering.

[Go to Exercise →](exercises/05-market-research/)

---

### Video 6: Content & Marketing
**"Your AI Content Workshop"**

Create content workflows, maintain brand voice across channels, and build a content repurposing system.

[Go to Exercise →](exercises/06-content-marketing/)

---

### Video 7: Prototyping Business Apps
**"From Idea to Working Prototype"**

Build simple web interfaces and dashboards. Learn the MVP mindset and when to ship.

[Go to Exercise →](exercises/07-prototyping/)

---

### Video 8: Capstone Project
**"Build Your Own Business Tool"**

Apply everything you've learned to build a custom tool for your own business idea.

[Go to Exercise →](exercises/08-capstone/)

---

## Resources

- [Claude Code Cheatsheet](resources/cheatsheet.md) — Quick reference for commands and patterns
- [Troubleshooting Guide](resources/troubleshooting.md) — Common issues and how to fix them
- [Capstone Project Ideas](resources/project-ideas.md) — Inspiration for your final project

---

## How to Use This Course

1. **Watch the video first** — Get the concepts and see the demo
2. **Follow along with the exercise** — Use the starter files provided
3. **Try the stretch goal** — Push yourself with the optional challenge
4. **Build on it** — Modify the tool for your own use case

### Time Commitment

- Each video: 30-60 minutes
- Each exercise: 15-30 minutes
- Total course: ~10-15 hours

---

## FAQ

**Do I need to know how to code?**
No. This course assumes zero coding experience. You'll learn to describe what you want in plain English.

**What if I get stuck?**
Check the [troubleshooting guide](resources/troubleshooting.md). Each exercise also includes a solution folder you can reference.

**Can I use this for my actual business?**
Absolutely. The tools you build are real and functional. Many students use their capstone projects in their businesses.

**Is Claude Code free?**
Claude Code itself is free. You'll need an Anthropic API key with credits (free tier available for learning).

---

## License

This course is open source under the MIT License. Feel free to use, modify, and share.

---

*Built with Claude Code — naturally.*
