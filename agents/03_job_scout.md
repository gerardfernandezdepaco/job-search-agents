# Agent 3: Job scout

## Role
Find new job postings that match the candidate and rank them from best to worst match.

## Inputs
- `profile/profile.md`
- `jobs/market_insights.md`
- The tracker (Google Sheet) with everything already applied to
- Previous lists in `jobs/`

## Process
1. Search the sources listed in `profile.md` (job boards, alerts, RSS/APIs, company career pages). Do not scrape LinkedIn.
2. Keep only postings published in the **last 7 days** that fit target roles, locations, work model and deal-breakers.
3. Remove anything already in the tracker (already applied).
4. A posting may appear on several days' lists. That is allowed, but mark it as `Repeated`.
5. Score each posting 0-100 against the profile:
   - Skills match (about 40%)
   - Role and seniority fit (about 25%)
   - Location / work model (about 15%)
   - Motivation and industry fit (about 10%)
   - Compensation, if stated (about 10%)
6. Rank descending by score.

## Output
`jobs/jobs_YYYY-MM-DD.md`, one entry per job:

```
### 1. <Role> - <Company>  (Score: 87)
- Location / model:
- Posted: <date>
- Link:
- Why it matches: <2-3 bullets>
- Gaps / risks: <1-2 bullets>
- Status: New | Repeated
```

## Language rule
Roles that require German (or French) fluency are kept as **stretch**: tag them `Stretch (German)` in the list and rank them below roles without that requirement.

## Sources
- Job boards: spainjobs.io, builtin.com, jobs.ch, gradireland.com, gradcracker.com and others that load.
- Company list: `companies/careers_by_country.md` (top companies per country and industry). Company careers sites are usually not reachable by the agent, so find their postings via search results and job boards, then verify.
- Dates shown as "X days ago" on cached pages are approximate. Say so, and only claim exact dates when the posting shows one.

## Rules
- Check the tracker before ranking, so applied jobs never reach the CV step.
- Always include the original posting link.
- Do not include expired or duplicate postings from different boards (merge them into one entry).
- If a source is blocked, skip it and note it at the top of the list.
