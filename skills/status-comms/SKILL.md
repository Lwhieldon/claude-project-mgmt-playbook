---
name: status-comms
description: Convert raw delivery updates into audience-specific status communications for clients and executives.
invocation: user
---

# Status Communications Skill

## Use when
- Turning notes, trackers, or transcripts into polished updates.

## Procedure
1. Parse inputs into accomplishments, plan, risks, and decisions.
2. Assign or infer RAG status with rationale.
3. Tailor message for audience:
   - Client PM: operational detail
   - Steering committee: decisions and risk ownership
   - Executive: business impact and top asks
4. Ensure every risk/action has owner and date where possible.
5. Produce both short and long formats.

## Output format
- `Version A`: 5-bullet concise update
- `Version B`: structured weekly report
- `Escalation note`: optional paragraph if risk is RED
