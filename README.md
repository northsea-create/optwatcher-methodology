# OPT Watcher Methodology

This repository documents how [OPT Watcher](https://optwatcher.com/en) turns a bounded snapshot of community-reported OPT timelines into planning ranges.

OPT Watcher is a free, no-signup planning tool. It compares an applicant's filing date and planned job start with separate estimates for:

- reported OPT approval;
- EAD card production and delivery;
- Regular and Premium Processing;
- Initial OPT and STEM OPT.

Try the calculator: [optwatcher.com/en](https://optwatcher.com/en)

Read the worked example: [Will Your EAD Arrive Before Your Job Starts?](https://optwatcher.com/en/opt-approval-timeline-guide)

## Current public snapshot

The October 2, 2026 snapshot contains:

| Measure | Count |
| --- | ---: |
| Source rows | 3,308 |
| Imported Reddit-linked timelines | 3,303 |
| Reported approvals | 2,411 |
| Reported card receipts | 676 |

Only rows retaining an original Reddit `r/f1visa` comment permalink were imported. OPT Pulse-only user submissions and anomalous date chains were excluded. The repository contains aggregated ranges only, not the original case-level records.

The machine-readable aggregate is available in [`data/community-estimates-2026-10-02.json`](data/community-estimates-2026-10-02.json).

## How the ranges are built

1. Split reports into four cohorts: Initial OPT Regular, Initial OPT Premium, STEM OPT Regular, and STEM OPT Premium.
2. For reported approvals, use the 50th-to-90th percentile of the latest sample: up to 150 Regular approvals or 250 Premium approvals.
3. For card delivery, calculate the 25th-to-75th percentile of reported calendar days from approval to card receipt.
4. Keep approval and card-in-hand as separate milestones.
5. Put both ranges on the same calendar as the user's planned job start.

For a pending Regular case, the Premium comparison uses the calculation date as a hypothetical Premium clock start. For an active Premium case, the user enters the applicable USCIS Premium clock-start date.

More detail: [`METHODOLOGY.md`](METHODOLOGY.md)

## What the result means

The output is a planning range built from historical, self-reported timelines. It is not:

- a personal probability of approval;
- official USCIS case status;
- a guarantee of approval or delivery;
- legal advice or employment authorization.

Applicants should confirm work eligibility with their DSO and official documents.

## Source

The aggregate was recomputed from the OPT Pulse public cases snapshot captured on October 2, 2026:

- Source: <https://opt-pulse.vercel.app/data/cases.json>
- Product: <https://optwatcher.com/en>

