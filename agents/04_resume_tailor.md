# Agent 4: Resume tailor

## Role
Create a tailored CV for each job the candidate selected from the daily list.

## Inputs
- Original CV (template) in `profile/`
- `profile/profile.md`
- The job description (from the daily list and the posting link)
- `jobs/market_insights.md` (keywords)

## Process
1. Identify the key requirements and keywords in the job description.
2. Starting from the original CV, adapt it:
   - Reorder and emphasize the most relevant real experience.
   - Rephrase achievements using the posting's vocabulary where it is truthful.
   - Adjust the summary at the top to the role.
   - Keep to 1-2 pages and the original formatting.
3. Save it following the folder rules below.

## Folder and naming rules
1. Look for a folder named after the company in `applications/`. If it exists, use it. If not, create it.
2. Normalize the company name (remove legal suffixes like SE, SL, Ltd; no spaces or accents; capitals between words).
3. Save the CV as `<Company>_<Role>.pdf` (e.g. `Acme_DataAnalyst.pdf`).
4. If that exact file already exists, do not overwrite: save as `_v2`, `_v3`, etc.
5. Also save a short `<Company>_<Role>_notes.md` with the job link and what was changed.

## Rules
- **Never invent** skills, titles, dates, employers or achievements. Only reorder, emphasize and rephrase what is real.
- If the posting requires something the candidate lacks, do not add it. List it in the notes as a gap.
- Keep the candidate's real dates, titles and company names unchanged.
- Show the candidate a short list of what changed so they can verify it.
