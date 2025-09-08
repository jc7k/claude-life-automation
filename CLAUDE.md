# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the Claude Life project - a personal productivity and automation system that leverages Claude's capabilities to create intelligent workflows for personal and professional development. The project focuses on building slash commands, subagents, and automated systems for tasks like weekly check-ins, daily journaling, newsletter research, and brain dump analysis.

**Created by:** Alex Finn - [YouTube Tutorial](https://youtu.be/wfiv67NixCY?si=p1atWlcUs8Ec522Z)

## Project Structure

```
.
├── claude-life-prompts.md  # Main collection of prompt templates and system designs
├── prompts/                 # Directory for organized prompt templates
├── .claude/                # (To be created) Claude-specific configuration
│   ├── commands/           # Slash commands
│   └── subagents/          # Specialized subagents
├── metrics/                # (To be created) Metrics tracking and reports
├── journal/                # (To be created) Daily journal entries
│   └── daily/             # Daily check-in files
├── newsletter/             # (To be created) Newsletter research and drafts
│   └── drafts/            # Newsletter draft files
└── braindumps/            # (To be created) Brain dump files and analysis
    └── analysis/          # Brain dump analysis reports
```

## Key Systems and Commands

### Weekly Check-in System
- Intelligently discovers relevant metrics based on project context
- Tracks progress with visual indicators and trends
- Generates actionable insights and recommendations
- Command: `/weekly-checkin`

### Daily Journal System  
- Personal reflection and planning tool
- Tracks mood, energy, accomplishments, and gratitude
- Analyzes patterns over time for personal growth insights
- Command: `/daily-checkin`

### Newsletter Research System
- Analyzes competitor newsletters for trending topics
- Identifies content gaps and opportunities
- Writes drafts in the user's voice
- Command: `/newsletter-research`

### Brain Dump Analyzer
- Extracts insights from stream-of-consciousness writing
- Identifies recurring themes and hidden connections
- Creates visual mind maps and action items
- Command: `/brain-dump-analysis`

### Daily Brief System
- Personalized news briefing based on user interests
- Filters for relevance and actionability
- Only includes stories from the past 7 days
- Command: `/daily-brief`

## Development Guidelines

### Creating New Commands
1. Place new slash commands in `.claude/commands/`
2. Follow the existing pattern of intelligent context discovery
3. Commands should adapt to the specific user, not use generic templates

### Creating New Subagents
1. Place specialized subagents in `.claude/subagents/`
2. Each subagent should have a focused expertise
3. Use visual elements (emojis, ASCII art, tables) for better readability

### Data Organization
- Metrics and reports go in `/metrics/`
- Journal entries go in `/journal/daily/` with format `YYYY-MM-DD.md`
- Newsletter drafts go in `/newsletter/drafts/`
- Brain dumps go in `/braindumps/` with analysis in `/braindumps/analysis/`

## Important Principles

1. **Context-Aware Intelligence**: Always analyze project context first before applying any templates or generating content
2. **Personalization**: Systems should adapt to each user's specific needs, not use generic approaches
3. **Visual Communication**: Use markdown tables, ASCII progress bars, emojis, and other visual elements to make reports engaging
4. **Progress Over Perfection**: Focus on encouraging progress and celebrating wins, however small
5. **Actionable Insights**: All analysis should lead to specific, actionable recommendations