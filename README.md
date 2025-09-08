# Claude Life - Personal Automation System

A collection of intelligent personal productivity commands and automation systems for Claude Code that adapt to your specific context and help you track progress, reflect on growth, and stay informed.

## 🎬 Credits

This system was created by **[Alex Finn](https://www.youtube.com/@AlexFinnOfficially)** and shared in his YouTube video: **[Watch the Tutorial](https://youtu.be/wfiv67NixCY?si=p1atWlcUs8Ec522Z)**

Check out Alex's video for a complete walkthrough of how to use these commands and see them in action!

## 🚀 Quick Start

All commands are available as slash commands in Claude Code. Simply type `/` followed by the command name.

## 📋 Available Commands

### `/weekly-checkin` - Weekly Progress Tracker
**When to use:** Once per week (e.g., Sunday evening or Monday morning)

**What it does:**
- Intelligently discovers what metrics matter to YOU based on your project files
- Tracks week-over-week progress with visual indicators
- Generates actionable insights and recommendations
- Creates beautiful reports with trends and momentum indicators

**Usage tips:**
- Run consistently on the same day each week
- Be honest with your metrics for accurate trend analysis
- Review the generated recommendations and act on them

**Output:** Saves to `/metrics/weekly-report-YYYY-MM-DD.md`

---

### `/daily-checkin` - Evening Reflection System
**When to use:** End of each day (evening routine)

**What it does:**
- Guides you through personal reflection questions
- Tracks mood, energy, accomplishments, and gratitude
- Analyzes patterns over time to identify what works
- Provides encouraging feedback and gentle suggestions

**Usage tips:**
- Make it part of your evening routine
- Keep responses brief but honest
- Review weekly patterns to optimize your schedule
- Note: This is different from `/daily-brief` which is for morning

**Output:** 
- Journal entry: `/journal/daily/YYYY-MM-DD.md`
- Analysis: `/journal/daily/YYYY-MM-DD-reflection.md`

---

### `/daily-brief` - Morning News Briefing
**When to use:** Start of each day (morning routine)

**What it does:**
- Analyzes your files to understand your interests
- Searches for news from the LAST 7 DAYS ONLY
- Filters for relevance and actionability
- Explains why each item matters to you specifically
- Suggests actions you could take

**Usage tips:**
- Run first thing in the morning
- Focus on the "Priority News" section
- Use the action summary to plan your day
- Pairs well with `/daily-checkin` in the evening

**Output:** Saves to `/daily-briefs/brief-YYYY-MM-DD.md`

---

### `/newsletter-research` - Newsletter Creator
**When to use:** When you need to write a newsletter

**What it does:**
- Analyzes competitor newsletters for trends
- Identifies content gaps and opportunities
- Writes complete 500-800 word drafts (not just outlines)
- Matches your writing voice from existing content
- Creates 3 subject line options

**Setup required:**
- Store competitor newsletter URLs in a file
- Have samples of your own writing available
- Create `/newsletter/drafts/` directory

**Usage tips:**
- Provide 3-5 competitor newsletter URLs for best results
- Review and personalize the draft before sending
- Test different subject lines with your audience

**Output:**
- Research: `/metrics/newsletter-research-YYYY-MM-DD.md`
- Draft: `/newsletter/drafts/newsletter-YYYY-MM-DD.md`

---

### `/brain-dump-analysis` - Thought Pattern Analyzer
**When to use:** After creating brain dump files or when you need clarity

**What it does:**
- Scans all your brain dump files
- Identifies recurring themes and patterns
- Finds hidden connections between ideas
- Creates visual mind maps
- Extracts your top realizations in YOUR words
- Generates action items you mentioned

**Setup required:**
- Create brain dumps in `/braindumps/` directory
- Write stream-of-consciousness style for best results

**Usage tips:**
- Write brain dumps without self-editing
- Run analysis weekly or when feeling stuck
- Review the "Top 10 Realizations" for insights
- Use extracted action items for task planning

**Output:** Saves to `/braindumps/analysis/analysis-YYYY-MM-DD.md`

---

## 🤖 Subagents (Backend Processors)

**Important:** These subagents are NOT standalone - they're automatically triggered by their parent commands. You don't need to interact with them directly.

### Command-Triggered Subagents

| Subagent | Triggered By | Purpose |
|----------|--------------|---------|
| `metrics-analyst` | `/weekly-checkin` | Creates visual progress reports with trends and recommendations |
| `daily-reflection` | `/daily-checkin` | Analyzes daily patterns for personal growth insights |
| `content-researcher` | `/newsletter-research` | Finds trending topics and content opportunities |
| `newsletter-writer` | `/newsletter-research` | Writes newsletter drafts in your voice |
| `insight-extractor` | `/brain-dump-analysis` | Identifies patterns and connections in brain dumps |
| `brain-dump-analyst` | `/brain-dump-analysis` | Creates visual summaries and action items |
| `interest-analyzer` | `/daily-brief` | Discovers your interests from project context |
| `news-curator` | `/daily-brief` | Finds and filters relevant news with explanations |

**Note:** The subagents work in sequence - for example, `/newsletter-research` first triggers `content-researcher` to analyze trends, then passes those insights to `newsletter-writer` to create the draft.

---

## 📁 Directory Structure

The system will create these directories as needed:

```
.claude/
├── commands/          # Slash command definitions
└── subagents/         # Backend processors

metrics/               # Weekly reports and metrics history
journal/              
└── daily/            # Daily check-ins and reflections

newsletter/
└── drafts/           # Newsletter drafts

braindumps/           # Your brain dump files
└── analysis/         # Analysis reports

daily-briefs/         # Morning news briefings
```

---

## 🎯 Recommended Workflows

### Daily Routine
**Morning:**
1. Run `/daily-brief` to get personalized news and set priorities
2. Review action items and plan your day

**Evening:**
1. Run `/daily-checkin` to reflect on the day
2. Review the generated insights and patterns

### Weekly Routine
**Sunday or Monday:**
1. Run `/weekly-checkin` to track progress
2. Review trends and adjust strategy
3. Run `/brain-dump-analysis` if you have new brain dumps

### Content Creation
**When needed:**
1. Write brain dumps throughout the week
2. Run `/brain-dump-analysis` for content ideas
3. Run `/newsletter-research` when ready to write

---

## 💡 Pro Tips

1. **Consistency is key:** Run daily commands at the same time each day for best pattern recognition

2. **Context matters:** The more project files and context you have, the better the commands adapt to your needs

3. **Brain dumps work best when:** 
   - Written stream-of-consciousness style
   - Done regularly (even 5 minutes daily)
   - Not self-edited or filtered

4. **Metrics tracking improves when:**
   - You track the same metrics consistently
   - You're honest about the numbers
   - You act on the recommendations

5. **Newsletter quality depends on:**
   - Quality of competitor URLs provided
   - Having your own writing samples available
   - Regular use to learn your voice

---

## 🔧 Customization

Each command and subagent is defined in markdown files that you can edit:
- Commands: `.claude/commands/[command-name].md`
- Subagents: `.claude/subagents/[subagent-name].md`

Feel free to modify them to better suit your specific needs!

---

## 📝 Notes

- All dates in file names use YYYY-MM-DD format
- Commands adapt to YOUR context - they don't use generic templates
- The system focuses on progress over perfection
- Visual elements (emojis, tables, progress bars) make reports engaging
- Everything is stored locally in your project directory