# International Student Mental Health – SQL Analysis

Exploratory analysis using PostgreSQL to examine whether the length of stay
affects the mental health diagnostic scores of international university students.

## Context

This is a guided project from **DataCamp**. The dataset, problem statement, and
column descriptions are provided by DataCamp. The original study surveyed students
at a Japanese international university (2018) and explored the link between length
of stay, social connectedness, acculturative stress, and depression.

The SQL query and the analysis/interpretation in this repository are my own work.

## Objective

Group international students by length of stay and compare their average scores on:
- **PHQ-9** (depression)
- **SCS** (social connectedness)
- **ASISS** (acculturative stress)

## Tools

- PostgreSQL

## Approach

Filtered the dataset to international students, grouped by length of stay, and
computed average diagnostic scores with `AVG`, rounded with `ROUND`, counted
students per group with `COUNT`, and ordered by length of stay.

## Key observations

- Most of the data is concentrated in stays of 1–4 years; longer stays have very
  few students (some groups have a single student), so those rows are not
  statistically reliable.
- Within the groups with enough data, average depression and acculturative stress
  scores tend to **increase** with longer stays during the first years.
- Social connectedness stays relatively flat.

> Note: this is an exploratory observation, not a causal conclusion. No significance
> testing was performed and group sizes are uneven.

## Files

- `notebook.ipynb` – full analysis with context, query, and output
- `students.csv` – dataset used for the analysis (provided by DataCamp)
