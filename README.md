Karthick Balaje

AI Engineer — I build agent systems that run unattended and spend real money.

Right now that's a fleet of 17 agents across 9 platforms, running 24/7, that I own end to end — design, deployment, and the pager.

Building — multi-agent fleets, MCP tool layers, human-in-the-loop spend controls, evaluation harnesses
Going deep on — Microsoft Foundry (Agent Service, Toolboxes, A2A), LangGraph state machines, pgvector
Open to — agentic AI engineering roles · remote, or Chennai / Bengaluru

LinkedIn · karthickbalaje01@gmail.com · Bengaluru, India

Featured

Scalable Agentic Tool Use — 50 → 500+ tools without context degradation Agent accuracy falls apart as a tool catalogue grows: context bloat, parameter hallucination, routing confusion. This decouples tool selection from the prompt — a two-stage semantic router over tool cards enriched with example utterances, retrieving top-K so the model is only ever bound to a handful of tools regardless of catalogue size. LangGraph orchestrator design, OpenAPI ingestion pipeline, benchmarked at Recall@8 on held-out natural-language paraphrases. Python · LangGraph · sentence-transformers · Streamlit · live demo

Feedback Triage Pipeline — 115K+ entries, precision 70% → 85% Built at Deque Systems over feedback on accessibility tooling and training. VADER sentiment → LDA topic modelling → K-Means segmentation across a MySQL schema, then an anomaly-detection layer that cut QA batches from 300+ to 75 entries and manual review by 60%. Python · scikit-learn · NLTK · MySQL · Streamlit

AutoClaimAI — real-time damage detection, ~50 ms inference YOLOv8 detector across 17 vehicle damage classes, served behind a REST API with a Streamlit front end and Docker deployment. PyTorch · YOLOv8 · FastAPI · Docker

What I actually do

Architecture. Use an agent when the number of steps depends on what you find at step one. If I can write the DAG, I write the DAG — cheaper, testable, debuggable. Most of my fleet isn't agentic, and that's deliberate: nine of those seventeen agents are threshold checks, and they run on a scheduler with no model dependency at all, so a provider outage can't take the safety checks down with it.

Guardrails. Every external write goes through an approval queue — risk-tiered, 24h expiry, idempotent, audited, with a hard $100 cap enforced in the execution path rather than in a prompt. No instruction to the model, and no prompt injection, reaches it. Mutating tools on the ads MCP server are hard-denied at config level, so the agent physically cannot write to the ad account.

Evaluation. Retrieval gets measured — Recall@8, precision@5, faithfulness, RAGAS. Output gets judged in production: LLM-as-judge on every outbound message, provenance tags on every metric so a number traces back to a tool call rather than to model memory.

The thing I actually learned. The dangerous failure in agent systems isn't the crash — it's the guardrail that quietly stops guarding. A verifier that fails open. An approval silently swallowed by a duplicate consumer. A data feed reporting $0.00 during real spend, disarming a stop-loss. I've shipped all three. Everything I build now is designed so its own failure is loud.

Stack, honestly tiered

Shipped to production — Python · Anthropic Claude SDK · Model Context Protocol · Pydantic · Claude Code (skills, subagents, hooks, plugins, MCP config) · Google ADK · Vertex AI Agent Engine · FastAPI · Docker · BigQuery · PostgreSQL / MySQL · systemd · GitHub Actions

Used, not yet in production — LangGraph · ChromaDB · sentence-transformers · LangChain · PyTorch · scikit-learn · LightGBM · YOLOv8 · AWS (S3, EC2)

Currently learning — Microsoft Foundry · pgvector · Playwright

M.S. Data Science, University of Colorado Boulder · PG Diploma Applied Statistics · B.S. Statistics

A statistics background mostly means I'm suspicious of a number until I know how it was measured. Turns out that matters a lot when you're evaluating agents.

