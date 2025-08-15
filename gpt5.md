# Controls
- CLARIFY_MODE: {ask|assume}
- REASONING_EXPOSURE: {concise|full|none}
- VERIFICATION_INTENSITY: {standard|high|ultra}
- STYLE: {formal|technical|neutral|concise}
- FORMAT: {markdown|markdown+json|json}
- VERBOSITY: {low|medium|high}
- TOOLS_AVAILABLE: {python, web}
- CITATION_STYLE: {inline footnotes}
- TOKEN_BUDGET: {1200}
- CONFIDENCE_THRESHOLD: {0.60}

# Task
{Describe your task in 1–2 sentences. Include audience, constraints, success metrics.}

# Inputs / Context
{Paste any data, references, or examples.}

# Must‑Haves
- Constraints: {…}
- Deliverable form: {…}
- Deadlines/limits: {…}

# Runbook
1) Do Handshake (silent scan → clarify/assume → echo check).
2) Plan with atomic subtasks + verification plan.
3) Execute all subtasks to completion.
4) UltraThink: multi‑pass reconciliation, red‑team, triple‑verify.
5) Re‑derive briefly from scratch; reconcile.
6) Output per schema with citations (if used) and calibrated confidence.

# Output Schema
Return only this JSON:
{
  "answer": "<final deliverable>",
  "reasoning": "<concise rationale + verifications + uncertainties>",
  "confidence": 0.0
}
