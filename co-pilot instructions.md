# Copilot Instructions — J4LStrategy Legal Document Repository

## Repository Overview

This is a legal document repository for a civil lawsuit filed in **Vanderburgh County, Indiana** (Indiana state court), managed by the plaintiffs. You (the AI agent) assist with document management, legal analysis, motion drafting, and case strategy. Always apply **Indiana law**, **Indiana Trial Rules**, and **Indiana Rules of Evidence** — not federal rules — unless explicitly instructed otherwise.

## First Steps for Every Task

1. **Read `agent_prompt.md`** at the repository root for full instructions on how this repository works, the directory structure, and the rules you must follow.
2. **Read the `agent_prompt.md`** in any directory you'll be working with for context-specific instructions.
3. **Check for new documents** — run `python scripts/index_documents.py --check-only` to see if there are unindexed documents. If so, update the index before proceeding.

## Key Rules (Summary)

- **NEVER quote directly from `plaintiff_notes/`** — these are privileged. Paraphrase and cite underlying evidence instead.
- **Always create a branch and PR** for tasks that produce new documents.
- **Place all drafts in `agent_work_products/`** — never place drafts directly in `motions_and_orders/`.
- **Use proper legal citation format** when drafting court filings, citing **Indiana Trial Rules**, **Indiana case law**, and **Vanderburgh County local rules**.
- **Anticipate opposing counsel's response** when drafting motions or providing strategy.

## Available Scripts

- `python scripts/index_documents.py` — Scan and update the document index.
- `python scripts/index_documents.py --check-only` — Check for changes without updating.
- `python scripts/export_index_html.py` — Export the index to a human-readable HTML file.
- `python scripts/parse_legal_pdf.py --input FILE --output-dir DIR --document-id ID` — Parse a legal PDF via Azure AI Document Intelligence into structured JSON and LLM Markdown.
