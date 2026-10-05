# Karthick Balaje

**AI engineer. I build LLM agents that are evaluated before they ship and governed once they're live.**

📍 Bengaluru, India · [LinkedIn](https://linkedin.com/in/karthickbalajege) · [karthickbalaje01@gmail.com](mailto:karthickbalaje01@gmail.com) · [Writing on Medium](https://medium.com/@karthickbalaje01)

**Now:** running a production LLM agent fleet for a US direct-to-consumer apparel brand: 21 scheduled jobs across 10 commerce and marketing APIs, every claim checked against live data before it reaches the founder, and a person approving every dollar of ad spend.

---

## Selected work

| Project | What it is | What it shows |
|---|---|---|
| [**ClaimLens**](https://github.com/kb2326/claimlens) | Car-damage claims triage. My own vision models measure the damage, a LangGraph agent reasons over the evidence and the policy wording, and fixed rules decide. Only a person can deny a claim. [Live showcase](https://huggingface.co/spaces/kb2606/claimlens) · [write-up](https://medium.com/@karthickbalaje01/i-built-an-ai-system-for-insurance-claims-where-the-ai-isnt-allowed-to-deny-you-9188ecdada8e) | Eval gate in CI on golden sets, 33 of 33 red-team attacks held, hybrid RAG over policy clauses with verified citations, 4 MCP servers with scoped tools, $0.010 per claim |
| [**cordilla-account-scoring**](https://github.com/kb2326/cordilla-account-scoring) | Turns an existing scoring model into a rep's morning: who to call, what to refresh first, what to leave, and what to say | Records cost and data quality on every run, and checks for the slow drift that broke the last scoring rollout |
| [**supplier-discovery-agent**](https://github.com/kb2326/supplier-discovery-agent) | A free-text buyer request becomes a ranked, verified top-5 supplier shortlist | Routes each part of a query to the right engine (vector, SQL filter, external API), fuses with RRF, scores with MCDA, verifies before ranking |
| [**agentic-tool-scaling**](https://github.com/kb2326/agentic-tool-scaling) | Design and prototype for an agent that works across 500+ tools | Two-stage semantic tool router, OpenAPI ingestion, hierarchical LangGraph orchestrator |

Earlier: [Proposal-ADK-search-Agent](https://github.com/kb2326/Proposal-ADK-search-Agent) (Google ADK, plan-execute-verify) · [feedback-analysis-dashboard](https://github.com/kb2326/feedback-analysis-dashboard) (NLP analytics) · [Smart-Grid-ML-Optimization-Project](https://github.com/kb2326/Smart-Grid-ML-Optimization-Project) (demand forecasting)

## How I build

- **Models measure, the agent reasons, rules decide.** Anything with consequences goes through code a person can read.
- **Evaluate the evaluator.** An LLM judge is only useful once you've measured how often it agrees with a human.
- **Build the outer loop first.** Specs, evals, tracing and approval rules before the clever part.

## Stack

- **Agents:** LangGraph · Model Context Protocol · Anthropic Claude SDK · Google ADK
- **Retrieval and evals:** hybrid search (BM25 + vectors) · LanceDB · golden sets · LLM-as-judge · red-teaming
- **Models:** PyTorch · YOLO11 segmentation · calibration
- **Shipping:** Python · FastAPI · Docker · GitHub Actions · DVC · GCP

---

*Building agents that know when **not** to act is harder than building agents that act.*
