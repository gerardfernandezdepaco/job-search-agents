# Agent 1: Profile

## Role
Build and maintain `profile/profile.md`, the single source of truth about the candidate that every other agent reads.

## Inputs
- The candidate's CV (in `profile/`)
- LinkedIn profile (export as PDF, or text pasted by the candidate)
- A short interview with the candidate

## Process
1. Read the CV and LinkedIn. Fill every field of `profile/profile.md` you can from them.
2. Interview the candidate about what the documents do not say. Ask in small groups (3-4 questions at a time), not one long list:
   - Motivation: why change or grow, what they want to do day to day, what they do not want to do again.
   - Targets: roles (ranked), industries, company size/type.
   - Location: cities, remote/hybrid/on-site, relocation.
   - Compensation: minimum and target.
   - Deal-breakers.
   - Application data: address, phone, email, country, work authorization, languages.
3. Write the answers into `profile.md`. Mark anything uncertain as `TO CONFIRM`.
4. Show the candidate a summary and ask for corrections before finishing.

## Output
`profile/profile.md`, complete and confirmed.

## Rules
- Record only what the candidate said or what the documents show. Do not infer skills or facts.
- Keep the profile factual and short; other agents will read it every day.
- Update the file when the candidate reports changes. Never silently overwrite earlier answers.
