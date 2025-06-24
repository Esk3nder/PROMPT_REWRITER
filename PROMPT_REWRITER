# PROMPT_REWRITER v1.2 — empirically‑tested scaffold
# Feed this wrapper + <<RAW_PROMPT>> to an LLM. It rewrites the raw prompt into the JSON schema below.

## Meta‑rules (read, do NOT output)
1. Preserve user intent; add **zero** creative content.
2. Use ≤ 70 % of the model’s max tokens (OpenAI *tiktoken* counting).  
   ‑ If over, insert top‑level key `"WARNING":"TOKEN_LIMIT_EXCEEDED"` in the JSON.
3. Omit `"ROLE_CONTEXT"` unless the task is stylistic or creative.
4. Perform **one** self‑review cycle: draft → critique → patch → final.
5. Output exactly the JSON block, then the AFTER_JSON instructions. No extra text.

## INPUT
<<RAW_PROMPT>>

## STRUCTURED_PROMPT  (output exactly this block)

{
  "DOMAIN_ANCHOR": "<field or discipline>",
  "TASK_DECLARATION": "<one‑sentence task (≤40 tokens)>",

  "FEW_SHOT": [
    {"input": "<example 1 minimal>", "output": "<desired answer 1>"},
    {"input": "<example 2>", "output": "<desired answer 2>"}
  ],

  "PRIMARY_OBJECTIVE": ["<key outcome 1>", "<key outcome 2>"],
  "SECONDARY_OBJECTIVES": ["<nice‑to‑have 1>", "<nice‑to‑have 2>"],

  "CONSTRAINTS": {
    "MUST": ["<mandatory requirement>"],
    "CANNOT": ["<forbidden>"],
    "PREFER": ["<preference>"]
  },

  "BACKGROUND": {
    "IMMEDIATE": ["<current state>"],
    "HISTORICAL": ["<brief history>"],
    "FUTURE": ["<implications>"]
  },

  "SUBTASKS": [],

  "EVALUATION": {
    "SUCCESS_CRITERIA": ["<definition of success>"],
    "FAILURE_CRITERIA": ["<definition of failure>"]
  },

  "OUTPUT_FORMAT": {
    "STRUCTURE": "<e.g. table, bullets>",
    "STYLE": "<tone/register>",
    "LENGTH": "<concise | medium | detailed>"
  },

  "VALIDATION": {
    "CHECKS": ["<verification steps>"],
    "STANDARDS": ["<reference guidelines>"]
  },

  "TAIL_RECAP": "<repeat TASK_DECLARATION verbatim or short hashed recap>"
}

## AFTER_JSON
CRITIQUE: Review the draft for correctness, clarity, brevity. List any issues.  
PATCH: Fix **all** listed issues, then stop.
