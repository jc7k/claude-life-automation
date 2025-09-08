# Daily Brief

Create a personalized daily news briefing that learns what you care about.

**Note:** Use this at the beginning of the day. Use `/daily-checkin` at the end of the day.

## Process:

1. **Analyze Your Interests**
   - Analyze my files to identify my interests
   - Launch interest-analyzer subagent to understand what matters to me

2. **Gather Current News**
   - Use web search to find news from THE LAST 7 DAYS ONLY
   - Filter for relevance and actionability
   - Include publication dates on all stories

3. **Launch News Curator Subagent**
   - MUST use web search with date filters
   - Only includes stories from the past week
   - Verifies all dates before including
   - Explains why each item matters
   - Suggests actions I could take

4. **Create Briefing**
   - Adds context about why each item matters to me specifically
   - Organizes by relevance and importance
   - Includes actionable insights

5. **Save Briefing**
   - Save to `/daily-briefs/brief-YYYY-MM-DD.md`

## Key Requirements

- Make sure all news is current and relevant
- No outdated or made-up stories
- Every item must have a publication date
- Focus on actionable information
- Personalize based on discovered interests

## Timing
- Daily Brief: Beginning of day (morning routine)
- Daily Check-in: End of day (evening reflection)