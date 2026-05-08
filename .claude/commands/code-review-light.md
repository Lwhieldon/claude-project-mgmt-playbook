---
description: Plain-English review of a code file or data artifact for delivery leads and project managers
---

# /code-review-light

## Purpose

Provides a plain-English review of a code file, SQL query, data pipeline, or technical artifact — written for a delivery lead who needs to understand what changed, why it matters, and what questions to ask the developer. Not a deep engineering review; a leadership-level read.

## Usage

```
/code-review-light $ARGUMENTS
```

`$ARGUMENTS` — File path to a code file, SQL script, configuration file, or data artifact.

## Inputs

- A code or data file (Python, SQL, JSON config, CSV schema, etc.)
- Optional: append context about what the code is supposed to do or what changed: `/code-review-light pipeline.py -- this was just modified to handle the new inventory feed`

---

Read the file at: $ARGUMENTS

Produce a leadership-level review with these sections:

**What This Does** (plain English):
2–4 sentences explaining what the code or artifact does, in terms a non-engineer can act on.

**What Changed or What's Notable:**
- Highlight the most significant logic, recent additions, or anything unusual
- Flag anything that looks like a workaround, hardcoded value, or "technical debt"

**Potential Risks:**
- What could go wrong? What assumptions is this code making?
- Any obvious security concerns (hardcoded credentials, unvalidated inputs)?
- Any dependencies on external systems or data that could break?

**Data or Output Impact:**
- What data does this touch? What does it produce?
- Would a bug here be silent (hard to detect) or loud (immediate error)?

**Questions to Ask the Developer:**
- 3–5 specific, well-formed questions a delivery lead should raise in the next technical review

This review is not a code quality audit. Focus on risk, clarity, and delivery impact.

---

## Example Output

**What This Does:**
This SQL script pulls all customer orders from the past 90 days, calculates each customer's total spend, and flags accounts that have spent more than $10,000 as "high value." The results are written to the `customer_segments` table used by the reporting dashboard.

**Potential Risks:**
- The 90-day filter is hardcoded (line 14). If this script runs in January after a system cutover, it will silently include pre-migration data.
- No error handling: if the `orders` table is unavailable, the script will fail silently and write nothing — the dashboard will show stale data with no alert.

**Questions to Ask the Developer:**
1. Is the 90-day window intentional, or should it be configurable? Who owns that parameter?
2. What happens to the dashboard if this script fails mid-run? Is there a fallback?
3. Has this been tested against the production data volume? How long does it take to run?
