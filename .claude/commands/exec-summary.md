# Purpose
Generate concise executive summaries for senior leadership and directors.

# Prompt
Create an executive summary based on provided artifacts using the default structure in `CLAUDE.md`.

Constraints:
- Max 220 words
- Business outcomes first
- Include only top risks/decisions
- Use confident, neutral tone

# Expected inputs
- Project files/folder
- Audience (director, CIO, steering committee)
- Time horizon (this week, this month, quarter)

# Example output
**Headline:** Program remains on track for Q3 launch with one controllable schedule risk.

The team completed core finance and sales data models and validated quality rules with business leads, improving readiness for UAT. The primary risk is delayed infrastructure access, which has compressed integration testing by one week; mitigation is active through parallel test execution and daily dependency tracking.

Top risks: (1) client environment readiness, (2) delayed approver response times, and (3) overlapping UAT resource demand. Proposed mitigations are in place with named owners and dated checkpoints.

Leadership decisions needed this week: approve temporary QA support extension through 17 July and confirm escalation path for unresolved access tickets by Wednesday. Immediate milestones are UAT dry run completion, cutover rehearsal plan sign-off, and steering review of go-live entry criteria.
