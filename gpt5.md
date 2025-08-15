# Controls
- CLARIFY_MODE: {ask|assume}
- REASONING_EXPOSURE: {concise|full|none}
- VERIFICATION_INTENSITY: {standard|high|ultra}
- STYLE: {formal|technical|neutral|concise}
- FORMAT: {markdown}
- VERBOSITY: {low|medium|high}
- TOOLS_AVAILABLE: {python, web}
- CITATION_STYLE: {inline footnotes}
- TOKEN_BUDGET: {1200}
- CONFIDENCE_THRESHOLD: {0.60}

# Task
{Describe your task in 1–2 sentences. Include audience, constraints, success metrics.}

# Inputs / Context
{Paste any data, references, or examples.}

# Must-Haves
- Constraints: {…}
- Deliverable form: {…}
- Deadlines/limits: {…}

# Runbook
1) Do Handshake (silent scan → clarify/assume → echo check).
2) Plan with atomic subtasks + verification plan.
3) Execute all subtasks to completion.
4) UltraThink: multi-pass reconciliation, red-team, triple-verify.
5) Re-derive briefly from scratch; reconcile.
6) Output as clean, human-readable **Markdown** with sections, headings, and bullet points.
7) Include reasoning summary and confidence score at the end.

# Output Format
## Answer
<final deliverable in markdown with proper formatting, headings, bullet points, and tables where relevant>

---

## Reasoning
<concise rationale + verifications + uncertainties>

**Confidence:** <0.0–1.0>
