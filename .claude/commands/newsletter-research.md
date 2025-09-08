# Newsletter Research

Analyze competitor newsletters and write drafts based on trending topics.

## Process:

1. **Gather Newsletter Sources**
   - Read newsletter URLs from my files (or ask me to provide them)
   - Fetch recent posts from those newsletters
   - Analyze my newsletter from the link in my files
   - Analyze the newsletters from my competitors in the links in my files

2. **Launch Content Researcher Subagent**
   - Analyzes competitor newsletters for trending topics
   - Identifies content gaps and opportunities
   - Finds time-sensitive angles
   - Passes insights to the newsletter-writer

3. **Launch Newsletter Writer Subagent**
   - Gets insights from the content-researcher
   - Writes 3 compelling subject line options
   - Creates a complete 500-800 word draft
   - Matches my writing voice based on my existing content
   - Includes practical takeaways
   - Adds a natural, soft CTA if relevant

4. **Save Output**
   - Save research to `/metrics/newsletter-research-YYYY-MM-DD.md`
   - Save draft to `/newsletter/drafts/newsletter-YYYY-MM-DD.md`

## Key Features

The system should:
- Analyze what's trending across multiple newsletters
- Write in MY voice (learn from my files)
- Create ready-to-send drafts, not just outlines
- Make subject lines that create curiosity
- Focus on value-first content that sounds authentic, not AI-generated

## Folder Structure
- `/newsletter/drafts/` for completed newsletters
- `/metrics/` for research reports