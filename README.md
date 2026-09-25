# Hospital Emergency Room Analysis

An Excel analysis of emergency room visits, wait times, department referrals, and patient satisfaction. The workbook includes the source table, supporting pivot summaries, and a dashboard.

## Project snapshot

| Measure | Result |
| --- | ---: |
| Visits | 9,216 |
| Average wait time | 35.3 minutes |
| Visits without a department referral | 5,400 (58.6%) |
| Visits referred to General Practice | 1,840 (20.0%) |
| Visits with a recorded satisfaction score | 2,517 (27.3%) |
| Average recorded satisfaction score | 5.0 / 10 |

The `Clean Date` column runs from April 1, 2019 through October 30, 2020. Each row has a distinct Patient ID in this workbook, so visit counts and distinct ID counts are both 9,216.

## Questions explored

- How many ER visits appear in the dataset?
- How long did patients wait on average?
- Which departments received the most referrals?
- What satisfaction scores were recorded, and how complete are those responses?

## Workbook

Open [hospital-er-analysis.xlsx](hospital-er-analysis.xlsx) in Microsoft Excel to explore the analysis and dashboard. GitHub does not display interactive Excel dashboards in its file preview.

| Sheet | Contents |
| --- | --- |
| `Hospital ER` | Source records and a cleaned date column |
| `Analysis` | Pivot summaries for referrals and other breakdowns |
| `DashBoard` | Excel dashboard and visualizations |
| `Sheet2` | Supporting headline measures |

## Findings

- The average wait across all 9,216 visits is **35.3 minutes**.
- **5,400 visits (58.6%)** have `None` as the department referral. Among named departments, **General Practice (1,840)** and **Orthopedics (995)** have the most referrals.
- Satisfaction scores are recorded for **2,517 of 9,216 visits**. The **5.0 / 10** average describes only those recorded responses; it is not an average for all visits.

## Method and limitations

- Counts and wait-time averages use the `Hospital ER` worksheet. The wait-time unit is minutes.
- The workbook contains both an original `Date` field and a `Clean Date` field. Some original `Date` values are stored as text and others as Excel dates; use `Clean Date` for the workbook's date-based analysis. Check ambiguous day/month source dates before using this data for operational decisions.
- Blank satisfaction cells mean **no score recorded** and are excluded from the satisfaction average. A recorded zero is a valid score.
- The meaning of `Patient Admin Flag` is not documented in the supplied data, so this project does not interpret it as an admission or discharge outcome.
- This is a portfolio analysis of a publicly shared dataset, not evidence about the performance of a real hospital. Patient IDs and names are present in the source workbook; avoid treating them as verified real patient details.

## Source

[Hospital Emergency Room Dataset on Kaggle](https://www.kaggle.com/datasets/drnimishadavis/hospital-emergency-room-dataset). Credit for the source dataset belongs to its Kaggle publisher. The analysis workbook in this repository is the project deliverable.
