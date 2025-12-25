# Exercise 6: Build a Content Repurposing Tool

**Time:** 25-30 minutes
**Difficulty:** Intermediate
**You'll build:** A system that transforms one piece of content into multiple formats

---

## The Business Problem

Your marketing team creates great content but struggles to maximize its reach. A single blog post could become a LinkedIn article, Twitter thread, email newsletter, and video script — but doing this manually takes hours. Let's automate content repurposing.

---

## What You'll Learn

- Working with content data at scale
- Maintaining brand voice across formats
- Creating multi-format content pipelines
- Analyzing content performance

---

## The Data

You have `content_library.csv` containing:
- 25 pieces of content (blogs, videos, case studies, etc.)
- Performance metrics (views, shares, conversions)
- Status and publication dates
- Topics and authors

---

## The Exercise

### Step 1: Start Claude Code

```bash
cd exercises/06-content-marketing
claude
```

### Step 2: Analyze Your Content Library

```
Read content_library.csv. Tell me:
- What types of content do we have?
- What are our top 5 performing pieces (by performance_score)?
- What topics resonate most with our audience?
```

### Step 3: Identify Repurposing Opportunities

```
Find published content with high performance scores (85+) that we could
repurpose into other formats. Show me the title, current format, and
suggest 2-3 other formats it could become.
```

### Step 4: Create a Repurposing System

Pick a top performer and repurpose it:

```
Take our top performing blog post and create:
1. A LinkedIn post (150-200 words, professional tone)
2. A Twitter thread (5-7 tweets, conversational, include a hook)
3. An email newsletter snippet (50-100 words with CTA)
```

### Step 5: Create a Repurposing Template

```
Create a reusable "content repurposing template" as a markdown file.
It should have prompts/sections for:
- Original content summary
- Key takeaways (3-5 points)
- LinkedIn version
- Twitter thread
- Email snippet
- Optional: Video script outline
```

### Step 6: Content Calendar Suggestions

```
Based on our content library and performance data, suggest a content
calendar for next month. Include:
- Which existing content to repurpose (and into what)
- Gaps in our content (topics we should cover)
- Best days to publish based on our data patterns
```

---

## Expected Outputs

### Repurposed Content Example

**Original:** "10 Ways to Boost Your Widget Efficiency" (blog post, 2100 words)

**LinkedIn Version:**
```
We analyzed 500+ widget workflows and found something surprising:

The most efficient teams don't work harder. They eliminate friction.

Here are the top 3 changes that made the biggest difference:

1️⃣ Automate the repetitive stuff (saved 4hrs/week avg)
2️⃣ Create templates for common tasks (reduced errors by 60%)
3️⃣ Set up smart notifications (no more checking constantly)

The full breakdown of all 10 techniques is on our blog [link]

What's your biggest efficiency win? 👇
```

**Twitter Thread:**
```
Thread: 10 widget efficiency hacks that actually work 🧵

1/ We analyzed 500+ workflows to find what separates efficient teams from the rest.

Here's what we found...

2/ Hack #1: Automate before you optimize

Most teams try to do things faster. The best teams ask "should we be doing this at all?"

Result: Average 4 hours saved per week.

[continues...]
```

---

## Stretch Goals

1. **Brand voice guide:** Create a document defining your brand voice with examples
2. **Performance predictor:** Based on patterns, predict which repurposed content will perform best
3. **Content gap analysis:** What topics have high performance but low content volume?
4. **Automated repurposing script:** Create a script that takes any blog post URL and generates all formats

---

## Key Content Patterns

### The Repurposing Multiplier
One piece of content can become:
- 1 long-form article → 5 LinkedIn posts
- 1 webinar → 10 social clips + 1 blog recap
- 1 case study → 3 quote graphics + 1 sales deck slide

### Maintaining Voice Across Formats
- **LinkedIn:** Professional but approachable
- **Twitter:** Casual, punchy, use threads
- **Email:** Personal, direct, clear CTA
- **Blog:** Comprehensive, SEO-friendly

### What to Repurpose
- High performers → More formats = more reach
- Evergreen content → Keeps giving value
- Timely content → Repurpose quickly before it's stale

---

## Solution Reference

Check the [solution folder](./solution/) for the repurposing template and example outputs.
