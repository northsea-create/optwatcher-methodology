# Methodology

## Purpose

Most timeline discussions answer one milestone at a time. OPT Watcher instead answers a planning question: does the reported approval-to-card window still fit before a proposed job start?

The model deliberately keeps these milestones separate:

1. the applicable processing clock start;
2. reported approval;
3. reported receipt of the physical EAD card;
4. the user's planned job start.

## Inclusion policy

The source snapshot contained 3,308 rows. A row was included only when it retained an original Reddit `r/f1visa` comment permalink. Five rows were skipped after validation, leaving 3,303 imported timelines.

The aggregate excludes OPT Pulse-only user submissions and anomalous date chains. It does not publish case-level records.

## Cohorts

Reports are separated by application and processing type:

- Initial OPT, Regular Processing;
- Initial OPT, Premium Processing;
- STEM OPT, Regular Processing;
- STEM OPT, Premium Processing.

This prevents a faster Premium sample from being mixed into a Regular planning range and keeps Initial and STEM timelines distinct.

## Approval range

The approval range is the 50th-to-90th percentile of the latest reported approvals in the cohort, using up to:

- 150 approvals for a Regular cohort;
- 250 approvals for a Premium cohort.

Pending cases are counted in the cohort totals shown to users but are not treated as completed approval durations.

## Card-delivery range

The card-delivery range is the 25th-to-75th percentile of reported calendar days from approval to card receipt. OPT Watcher adds this interval after the approval range rather than treating approval as the finish line.

## Premium clock

For a report in the source data, the Premium clock uses the latest applicable filing, Premium request, biometrics, or RFIE milestone available in that report.

For a user's pending Regular case, the comparison starts a hypothetical Premium clock on the calculation date. For an already active Premium case, the user supplies the applicable USCIS clock-start date.

## Interpretation

The range is descriptive, not predictive for a specific person. Community reports can be incomplete, late, duplicated at the source, or unrepresentative of all applicants. New outcomes can move the displayed range.

Use the result to prepare a planning conversation. Do not use it as official case status, legal advice, or proof of authorization to work.

Try the decision calculator at [OPT Watcher](https://optwatcher.com/en).

