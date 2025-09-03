# LLM with Python — Beginner Labs (Google Colab)

A self-paced set of **beginner-friendly labs** to learn practical Large Language Model (LLM) skills using **Python** and **Google Colab**.  
No prior ML background required—each lab is guided and runnable end-to-end.

---

## Who is this for?
- Students and developers **new to LLMs**
- Anyone who wants hands-on practice with **prompting**, **code assistance**, **RAG**, and **fine-tuning**
- Learners who prefer **Colab** (no local setup needed)

---

## What’s included

- **Lab 1 – Prompting an LLM**
  - Roles (system/user), constraints, few-shot examples
  - Temperature & max_tokens
  - Reusable helper functions
- **Lab 2 – Code Review Assistant**
  - Detect bugs/style/security issues
  - Generate unified diff patches & pytest tests
  - Batch review to simulate a pull request
- **Lab 3 – RAG Basics**
  - Chunk text → embeddings → cosine similarity search
  - Answer with **context grounding** and **citations**
- **Lab 4 – Fine-Tuning Demo**
  - **Option A (OpenAI SFT):** Create JSONL dataset → run fine-tune job → use tuned model  
  - **Option B (Local LoRA/PEFT):** Train adapters on a tiny open model in Colab GPU

> Tip: Start with **Lab 1** in order. Each lab is self-contained and takes ~20–40 minutes.

---

## 🚀 Open in Google Colab

| Lab | Description | Launch |
|---|---|---|
| Lab 1 | Prompting, roles, constraints, few-shot, temperature | <a href="https://colab.research.google.com/github/antrixsh/llm-python-colab-beginner-labs/blob/main/notebooks/Lab1_Prompting_with_Python_Colab.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| Lab 2 | Code Review Assistant (findings, diffs, pytest, PR batch) | <a href="https://colab.research.google.com/github/antrixsh/llm-python-colab-beginner-labs/blob/main/notebooks/Lab2_Code_Review_Assistant_Colab.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| Lab 3 | RAG Basics (chunk → embed → search → cite) | <a href="https://colab.research.google.com/github/antrixsh/llm-python-colab-beginner-labs/blob/main/notebooks/Lab3_RAG_Basics_Colab.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| Lab 4 | Fine-Tuning (OpenAI SFT or local LoRA/PEFT) | <a href="https://colab.research.google.com/github/antrixsh/llm-python-colab-beginner-labs/blob/main/notebooks/Lab4_Fine_Tuning_Demo_Colab.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

> Replace `<YOUR_GITHUB_USER_OR_ORG>` and `<YOUR_REPO_NAME>` after pushing notebooks to the `main` branch.

---

## Prerequisites

- **OpenAI API key** (needed for Labs 1–3 and Lab 4 Option A):  
  Create one at https://platform.openai.com/account/api-keys  
  You’ll paste it in Colab when prompted (not stored in the notebook).
- **Colab GPU** (only for Lab 4 Option B — LoRA/PEFT):  
  *Runtime → Change runtime type → GPU*

---

## Quick Start (Colab)

1. Click **Open in Colab** for a lab above.
2. Run cells top-to-bottom; provide your OpenAI API key when asked.
3. Follow the inline instructions and notes in each lab.

---

## Local (non-Colab) Setup (optional)

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
export OPENAI_API_KEY=sk-... # Windows PowerShell: $env:OPENAI_API_KEY="sk-..."

```

---
## 📚 Learning Path

1. **Lab 1 — Prompting Fundamentals (20–30 min)**
   - Goals: system vs user roles, constraints, few-shot, temperature/max_tokens
   - Outcome: predictable, well-structured responses
   - ✅ Checkpoint: reproduce the same output with temperature `0.2`

2. **Lab 2 — Code Review Assistant (25–40 min)**
   - Goals: detect bugs/style/security issues, generate diffs & pytest tests, batch review (PR-like)
   - Outcome: a JSON report of issues + a minimal unified diff + basic unit tests
   - ✅ Checkpoint: run the lab on your own snippet and get at least 1 actionable issue

3. **Lab 3 — RAG Basics (30–45 min)**
   - Goals: chunk → embed → cosine search → answer with **citations**
   - Outcome: grounded answers that reference retrieved context
   - ✅ Checkpoint: replace toy docs with 1–2 of your own `.txt` files and see citations update

4. **Lab 4 — Fine-Tuning (40–60 min)**
   - **Option A (OpenAI SFT):** create JSONL → fine-tune → use tuned model  
   - **Option B (Local LoRA/PEFT):** adapter-based training on `distilgpt2` (GPU recommended)
   - Outcome: responses aligned to your preferred **style/format**
   - ✅ Checkpoint: tuned model/adapters produce consistent docstring/type-hint style

> **Tip:** Start with Lab 1 and move sequentially. Labs are independent but build intuition cumulatively.

---

## ❓ FAQ

**Q1. Do I need prior ML experience?**  
No. Each notebook is guided and runnable end-to-end in Google Colab.

**Q2. Do I need a GPU?**  
Only for **Lab 4 Option B (LoRA/PEFT)**. All other labs work on CPU.

**Q3. Do I need an API key?**  
Yes, for **Labs 1–3** and **Lab 4 Option A (OpenAI SFT)**. You’ll paste it securely in Colab when prompted (not stored in the notebook).

**Q4. Which model should I use?**  
Default notebooks use small, cost-efficient models (e.g., `gpt-4o-mini`) and `text-embedding-3-small` for embeddings. You can change them based on availability and cost.

**Q5. How much will it cost?**  
Costs are usually low for small prompts/embeddings in these labs. Keep an eye on your provider dashboard; reduce tokens, use smaller models, or shorter contexts to save.

**Q6. I get “module not found” or SDK errors in Colab.**  
Run the **install** cell first; then **Runtime → Restart runtime** (if needed) and re-run in order.

**Q7. I see “rate limit” or “quota exceeded” errors.**  
Wait a minute and retry, or reduce batch size / token counts. Consider a more generous plan if you hit limits frequently.

**Q8. My outputs vary between runs.**  
Lower `temperature` (e.g., `0.2`) for more deterministic results. Add **few-shot** examples to lock the format.

**Q9. Can I use my own documents in RAG?**  
Yes. In **Lab 3**, use the upload cell to add `.txt` files, then re-embed. For PDFs/HTML, you’ll need an extraction step (not included).

**Q10. Where are my secrets stored?**  
API keys are read into environment variables in the current Colab session only. Do **not** commit keys to GitHub.

**Q11. Can I run locally without Colab?**  
Yes. Use `requirements.txt`, set `OPENAI_API_KEY`, and open notebooks in Jupyter/VS Code. GPU is optional except for **LoRA**.

**Q12. Should I use RAG or fine-tuning?**  
- **RAG** for fresh, factual knowledge from your docs.  
- **Fine-tuning** for style, format, guardrails, or domain-specific phrasing.  
Many teams combine both.

**Q13. How big should my fine-tune dataset be?**  
For noticeable gains, target **100–1000+** high-quality, consistent examples. The lab uses a tiny set only to illustrate mechanics.

**Q14. Can I extend the labs?**  
Yes—add CI hooks, logging, evals, and swap toy data for real project data. PRs to improve clarity or add datasets are welcome.
