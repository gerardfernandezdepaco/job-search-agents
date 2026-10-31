# Tracker schema

**Live tracker:** your own Google Sheet (create it from this schema; see the README).
Spreadsheet ID: `<YOUR_SPREADSHEET_ID>` (sheet tab `Tracker`, header in row 1, data from row 2, formulas pre-filled to row 201).

`tracker/job_tracker.xlsx` is an offline copy with the same layout (backup).

## Columns

| Col | Name | Description |
|-----|------|-------------|
| A | # | Row number (automatic) |
| B | Position | Job title |
| C | Company | Normalized company name (same as the folder name in `applications/`) |
| D | Application date | YYYY-MM-DD |
| E | Link | Posting URL |
| F | Match score | 0-100, from the Job scout |
| G | Advanced to next phase? | Yes / No / Pending |
| H | Interview? | Yes / No / Pending |
| I | Technical test? | Yes / No / Pending |
| J | Offer? | Yes / No / Pending |
| K | Stage reached | Applied / Screening / Interview / Technical test / Offer |
| L | Status | Open / Closed |
| M | Progress % | Automatic, from Stage reached (table in sheet `Lists`) |
| N | Progress bar | Automatic. Green if Open, red if Closed |
| O | Notes | Free text |
| P | CV file | Path of the tailored CV in `applications/` |

## Stages and progress

| Stage reached | Progress |
|---------------|----------|
| Applied | 20% |
| Screening | 40% |
| Interview | 60% |
| Technical test | 80% |
| Offer | 100% |

Closed opportunities: set Status = Closed and keep Stage reached as the last stage. The row turns red and the bar keeps the progress reached.

## Rules
- One row per company + role. Check B and C before adding.
- Applications are recorded in order (new rows at the bottom).
- Never delete rows; close them instead.
- Row 2 is an example row (yellow). Delete or overwrite it with the first real application.

## Notes for the Tracker agent
- Write only to columns B-L and O-P. Columns A, M and N are formulas; never overwrite them.
- To add an application, write into the first row where column C (Company) is empty.
- The progress bar (N) is a SPARKLINE: green if Status = Open, red if Closed.
