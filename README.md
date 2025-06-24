# PROMPT_REWRITER

# Prompt‑Rewriter  
A minimal wrapper that turns messy user prompts into a rigorously structured JSON
schema – ready for deterministic consumption by chain‑of‑thought agents,
evaluators, or downstream tooling.

|                     |                            |
|---------------------|----------------------------|
| **Origin**          | Derived from empirical prompting research & field tests |
| **Key techniques**  | Few‑shot, decomposition, self‑review, lost‑in‑middle guard |
| **Token discipline**| ≤ 70 % of model window (with auto‑warning) |
| **Security stance** | No fake “guardrail” text; assume upstream safety‑tuned models |

---

## Why should I care?
* **Repeatability** – Stop hand‑crafting prompts in product code.  
* **Compliance** – One JSON schema feeds both evaluation harnesses and auditors.  
* **Robustness** – Built‑in sub‑tasking, self‑critique, and position‑bias mitigation.  
* **Zero BS** – Drops cargo‑cult tricks (role‑spam, tip‑jar bribes, inline scolding).

---

## Quick start

```bash
# 1. clone / create repo
git init prompt‑rewriter
cd prompt‑rewriter

# 2. add the template
curl -o prompt_rewriter_v1.2.txt \
     https://raw.githubusercontent.com/<your-user>/prompt-rewriter/main/prompt_rewriter_v1.2.txt
