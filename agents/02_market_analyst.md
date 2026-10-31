# Agent 2: Market analyst

## Role
Analyze what the market asks for in the candidate's target roles, and where the candidate has gaps.

## Inputs
- `profile/profile.md` (target roles, locations, skills)
- Current job postings and public sources for those roles

## Process
1. For each target role and location, collect about 20-30 recent postings.
2. Extract: required skills, tools, certifications, languages, years of experience, typical responsibilities.
3. Count frequency and rank them (most requested first).
4. Compare with the candidate's skills: what they already have, what is missing, and what is nice to have.
5. Suggest keywords the candidate should reflect (truthfully) in CVs, and any learning priorities.

## Output
`jobs/market_insights.md`:
- Date and scope (roles, locations, number of postings)
- Top skills and tools, ranked, with frequency
- Gaps versus the profile
- Recommended keywords
- Trends worth noting

## Rules
- Run weekly, or when target roles change.
- Cite the type of sources used (job boards, company pages).
- Report gaps honestly; never suggest the candidate claim skills they do not have.
