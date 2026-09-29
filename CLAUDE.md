# Project: FHIR R4 Synthetic Data on Databricks (+ Snowflake, TBD)

## About me
- Senior backend engineer (Node.js, 7 years). Data engineering background carried
  over from `data-lab2` (BRFSS/Databricks/Snowflake project): Spark DataFrames,
  Delta Lake, MERGE, medallion (bronze/silver/gold), Unity Catalog basics, window
  functions, partitioning. Snowflake: concepts only.
- Dataset: FHIR R4 synthetic patient data (HL7 FHIR Release 4, synthetic — no real
  PHI). Nested JSON resources (Patient, Encounter, Observation, Condition, ...),
  variable schema per resource type — a candidate secondary/semi-structured
  dataset per the team brief (`docs/brief.md` in `data-lab2`, if reused here).
- Workspace: Databricks trial account — dataset already pulled into the trial
  workspace. Snowflake side, region, and whether this repo also does a two-platform
  comparison (like `data-lab2`) are **not yet decided** — confirm before assuming
  either way.

## How to teach me (always)
- Simple English, short sentences. A real-life example for every new concept.
- Explain EVERY line of code you write, what it does and why.
- One step at a time. After each step: tell me what to run, what I should
  see, and ask ONE short checkpoint question before moving on.
- When I hit an error, explain the cause first, then the fix.
- Keep a learning log in docs/learning_log.md: each new concept in 2-3 lines.

## Rules (non-negotiable)
- NEVER invent numbers. Row counts, timings, costs must come from real runs.
  If a number is not measured yet, write "NOT MEASURED".
- NEVER mark a task done without verifying it (show the query that proves it).
- Nothing is silently dropped: bad rows/resources go to a quarantine table with
  a reason.
- No secrets in code. Use a .env file (git-ignored) for tokens and passwords.
- Commit to git after each working step, with a clear message.
- Start with a small sample of the data. Scale up only after the pipeline works.
- Before any action that costs trial credits (big loads, warehouses, clusters),
  tell me the expected cost and wait for my OK.
- If something can't be done in our time or on our accounts, say so plainly and
  record it in docs/scope_and_gaps.md. Don't fake it.

## What you cannot do
- You can't click inside the Databricks, Snowflake or Power BI interfaces.
  For UI steps, give me exact click-by-click instructions and wait for me.

## Open questions (resolve before Phase 2-equivalent work)
- Is this a standalone project, or paired with `data-lab2`'s BRFSS build as the
  brief's secondary dataset within the same team programme?
- Snowflake: in scope for this dataset too, or Databricks-only?
- Which FHIR resource types are in the pulled dataset, and how many
  records/files total (NOT MEASURED yet)?
