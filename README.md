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

## Open in Google Colab

| Lab | Description | Launch |
|---|---|---|
| Lab 1 | Prompting, roles, constraints, few-shot, temperature | <a href="https://colab.research.google.com/github/<YOUR_GITHUB_USER_OR_ORG>/<YOUR_REPO_NAME>/blob/main/notebooks/Lab1_Prompting_with_Python_Colab.ipynb" target="_blank">Open in Colab</a> |
| Lab 2 | Code Review Assistant (findings, diffs, pytest, PR batch) | <a href="https://colab.research.google.com/github/<YOUR_GITHUB_USER_OR_ORG>/<YOUR_REPO_NAME>/blob/main/notebooks/Lab2_Code_Review_Assistant_Colab.ipynb" target="_blank">Open in Colab</a> |
| Lab 3 | RAG Basics (chunk → embed → search → cite) | <a href="https://colab.research.google.com/github/<YOUR_GITHUB_USER_OR_ORG>/<YOUR_REPO_NAME>/blob/main/notebooks/Lab3_RAG_Basics_Colab.ipynb" target="_blank">Open in Colab</a> |
| Lab 4 | Fine-Tuning (OpenAI SFT or local LoRA/PEFT) | <a href="https://colab.research.google.com/github/<YOUR_GITHUB_USER_OR_ORG>/<YOUR_REPO_NAME>/blob/main/notebooks/Lab4_Fine_Tuning_Demo_Colab.ipynb" target="_blank">Open in Colab</a> |

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
