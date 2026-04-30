# From Vibe-Coded MVP to Production-Grade Agentic AI

**Date:** 2025-12-20
**Venue:** Pune
**Speaker:** Deepak Agarwal and Niteen Badgujar

## Synopsis

Most agentic AI talks dwell on the top 10% — the prompt, the model, the magic moment when it answers correctly. Production systems don't fail there. They fail in the other 90%: when the MCP server is down, when the response leaks PII, when the conversation drops mid-flight, when the agent hallucinates a refund it has no authority to issue.

This talk starts with a vibe-coded multi-agent customer-service system (Triage → FAQ / Order / RAG → Tone, with a Human-in-the-Loop step) and systematically engineers it for production across four pillars, each with a working hands-on demo:

1. **Observability** — distributed tracing with OpenTelemetry, Jaeger, and LangSmith. Spans, traces, and the waterfall view of agent execution.
2. **RAG groundedness** — Pinecone-backed retrieval, citations, user feedback loops, and online + offline evaluation with `ragas` (faithfulness, answer relevancy, context precision, response groundedness).
3. **State management & HITL durability** — LangGraph PostgreSQL checkpointers, `interrupt_before` for human escalation, conversations that survive deploys and crashes.
4. **Guardrails & policy enforcement** — defense-in-depth with PolicyIn (OpenAI Moderation + Microsoft Presidio for PII redaction) and PolicyOut (block toxic AI output, redact AI-generated PII, full audit trail).

Closes with Simon Willison's **Lethal Trifecta** (private data + external communication + untrusted content) as the framework that should guide every production-AI decision.

## Target audience

- Engineers who have shipped a chatbot or agent prototype and now have to operate it.
- Architects and tech leads evaluating LangGraph / LangChain for production agentic systems.
- Anyone who has demoed a vibe-coded agent and felt the gap between "it works on my machine" and "it works at 2 AM under load with adversarial input".

Assumes working familiarity with Python and large language model APIs. No prior LangGraph experience required.

## Stack

LangGraph · LangChain · OpenAI · Pinecone · PostgreSQL · Microsoft Presidio · OpenTelemetry · Jaeger · LangSmith · Gradio · `ragas`

## What's in this folder

- `slides.pptx` — final deck delivered at the venue
- `diagrams/Production-Grade-System.png` — the architecture diagram referenced throughout
- `demo/demo-code/` — five-step working progression: `1-initial-setup` → `2-observability` → `3-rag` → `3-HITL-state` → `4-guardrails`. Each step builds on the previous one without modifying earlier folders.
- `recording.md` — recording status
- `resources.md` — references and further reading
