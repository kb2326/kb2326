<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a7d4a,100:134e4a&height=170&section=header&text=Karthick%20Balaje&fontSize=44&fontColor=ffffff&fontAlignY=36&desc=AI%20engineer%20%C2%B7%20LLM%20agents%20that%20are%20evaluated%20before%20they%20ship&descSize=16&descAlignY=58" width="100%" alt="Karthick Balaje, AI engineer"/>

<p align="center">
  <a href="https://linkedin.com/in/karthickbalajege"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://medium.com/@karthickbalaje01"><img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" alt="Medium"/></a>
  <a href="mailto:karthickbalaje01@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Bengaluru,%20India-555555?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Bengaluru, India"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=500&size=17&duration=3200&pause=1200&color=0A7D4A&center=true&vCenter=true&width=640&lines=Models+measure%2C+the+agent+reasons%2C+rules+decide.;Every+number+comes+with+the+code+that+computed+it.;Evaluate+the+evaluator+before+you+trust+it." alt="Models measure, the agent reasons, rules decide. Every number comes with the code that computed it. Evaluate the evaluator before you trust it."/>
</p>

<p align="center"><b>I build LLM agents that are evaluated before they ship and governed once they're live.</b></p>

<table align="center">
<tr>
<td align="center"><b>1.00</b><br/><sub>escalation recall<br/>ClaimLens</sub></td>
<td align="center"><b>33 / 33</b><br/><sub>red-team attacks held<br/>ClaimLens</sub></td>
<td align="center"><b>1.00 / 0.91</b><br/><sub>knockout recall / precision<br/>Grant Capture</sub></td>
<td align="center"><b>0</b><br/><sub>invented facts in drafts<br/>Grant Capture</sub></td>
<td align="center"><b>29 / 32</b><br/><sub>labelled failures fixed<br/>Health Agent</sub></td>
</tr>
</table>

---

### 🚀 Now

- **In production:** an LLM agent fleet for a US direct-to-consumer apparel brand. It runs 21 scheduled jobs across 10 commerce and marketing APIs, checks every claim against live data before it reaches the founder, and has a person approve every dollar of ad spend.
- **Just shipped:** the [Calibrated Health Agent](https://github.com/kb2326/calibrated-health-agent) is public: an agent on my own health data with a web app, an eval suite and a CI gate (below).
- **Research:** a pre-registered study of Gemma 4 coding agents, public with its paper.

<table>
<tr>
<td width="50%" valign="top">

#### 🫀 [Calibrated Health Agent](https://github.com/kb2326/calibrated-health-agent) <sub><img src="https://img.shields.io/badge/live-open_source-0a7d4a?style=flat-square" alt="Live, open source"/></sub>
An AI agent you talk to about your own wearable and journal data. It plans, writes SQL or Python, runs it in a sandbox, and **every number links to a receipt you can re-run**. A code check, not a prompt, flags any figure no tool computed.

- One ReAct agent with thinking and 14 tools on Google ADK; specialists as tools
- **265 eval cases**, my own labels on 110 answers, a red team and a **CI gate on every PR**
- After error analysis and a redesign, **29 of 32** labelled failures answered better
- Web app over **AG-UI**: streamed steps, tappable receipts, live-location weather, behind Google sign-in
- **Seven forecasters** make sealed daily predictions, hash-chained and [published](https://github.com/kb2326/cha-ledger-log)
- Runs on GCP (Cloud Run, Terraform) for **under $1/month**

[Code](https://github.com/kb2326/calibrated-health-agent) · [Forecast scoreboard](https://kb2326.github.io/cha-ledger-log/)

`Google ADK` `Gemini` `AG-UI` `Next.js` `Vertex AI` `Terraform`

</td>
<td width="50%" valign="top">

#### 🧪 [Asking vs. Adding a Stage](https://github.com/kb2326/gemma4-ask-or-enforce) <sub><img src="https://img.shields.io/badge/paper-submitted-0a7d4a?style=flat-square" alt="Paper submitted"/></sub>
My paper for Kaggle's **Gemma 4 Developer Agent** competition (paper track): *A Pre-Registered Test on a Gemma 4 Coding Agent.* Gemma 4 31B fixes real GitHub issues within a fixed 4.5-minute budget; I compared prompt rules with a planning stage.

- Designed on 30 tasks, then tested **pre-registered claims once on 41 held-out tasks**
- Prompt rules are followed to the letter (**20/20 vs 0/25**), not in intent
- A planning-stage gain seen in development **did not replicate**, and the paper says so
- Every table recomputed from per-task results in a public notebook

[Code](https://github.com/kb2326/gemma4-ask-or-enforce) · [Reproduce the tables](https://www.kaggle.com/code/karthickbalaje/asking-vs-adding-a-stage-reproduce-tables)

`Gemma 4` `Google ADK` `vLLM` `Kaggle` `Pre-registration` `Paired statistics`

</td>
</tr>
</table>

---

### 🧩 Selected work

<table>
<tr>
<td width="50%" valign="top">

#### 🚗 [ClaimLens](https://github.com/kb2326/claimlens)
Car-damage claims triage. My own vision models measure the damage, a LangGraph agent reasons over the evidence and the policy wording, and fixed rules decide. **Only a person can deny a claim.**

- Damage segmentation mask mAP50 **0.733** (course baseline: 0.137)
- Escalation recall **1.00** · **$0.010** per claim
- **33 of 33** red-team attacks held · eval gate in CI

[Live showcase](https://huggingface.co/spaces/kb2606/claimlens) · [Write-up](https://medium.com/@karthickbalaje01/i-built-an-ai-system-for-insurance-claims-where-the-ai-isnt-allowed-to-deny-you-9188ecdada8e)

`YOLO11` `LangGraph` `MCP` `Hybrid RAG` `DVC`

</td>
<td width="50%" valign="top">

#### 📑 [Grant Capture Agent](https://github.com/kb2326/grant-capture-agent)
Finds federal funding a small R&D firm can actually win, rules out the ones it can't (quoting the clause and page), and drafts proposals from the company's own evidence.

- Knockout recall / precision **1.00 / 0.91**
- Drafts: **10 of 10** true gaps flagged, **0** invented
- Every module built twice; ablations picked what ships, and misses are reported

`Google ADK` `Gemini` `Corrective RAG` `pgvector` `MCP`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 📈 [cordilla-account-scoring](https://github.com/kb2326/cordilla-account-scoring)
Turns an existing scoring model into a rep's morning: who to call, what to refresh first, what to leave, and what to say.

- Logs cost and data quality on every run
- Watches for the slow drift that broke the last scoring rollout

`Python` `Claude` `LangSmith`

</td>
<td width="50%" valign="top">

#### 🏭 [supplier-discovery-agent](https://github.com/kb2326/supplier-discovery-agent)
Turns a free-text buyer request into a ranked, verified top-5 supplier shortlist.

- Routes each part of a query to the right engine (vector, SQL, graph, external API)
- Fuses results with RRF, scores them with MCDA, and verifies before ranking

`Claude` `Vector search` `SQL` `Graph`

</td>
</tr>
<tr>
<td colspan="2" valign="top">

#### 🧰 [agentic-tool-scaling](https://github.com/kb2326/agentic-tool-scaling)
Design and prototype for an agent that works across 500+ tools: a two-stage semantic tool router, OpenAPI ingestion, and a hierarchical LangGraph orchestrator. `LangGraph` `OpenAPI` `Semantic routing`

</td>
</tr>
</table>

<details>
<summary><b>Earlier work</b></summary>

- [feedback-analysis-dashboard](https://github.com/kb2326/feedback-analysis-dashboard): sentiment analysis, topic modeling and user segmentation (Streamlit, scikit-learn, Plotly)
- [Smart-Grid-ML-Optimization-Project](https://github.com/kb2326/Smart-Grid-ML-Optimization-Project): energy demand forecasting pipeline

</details>

---

### 🧭 How I build

> **Models measure, the agent reasons, rules decide.** Anything with consequences goes through code a person can read.
>
> **Evaluate the evaluator.** An LLM judge is only useful once you've measured how often it agrees with a human.
>
> **Build the outer loop first.** Specs, evals, tracing and approval rules come before the clever part.
>
> **Publish the losses.** Pre-register the test, report the baseline, and keep the result even when the simple rule wins.

---

### 🛠️ Stack

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch,fastapi,react,nextjs,ts,postgres,docker,githubactions,gcp,terraform&perline=11" alt="Python, PyTorch, FastAPI, React, Next.js, TypeScript, Postgres, Docker, GitHub Actions, GCP, Terraform"/>
</p>

| | |
|---|---|
| **Agents** | ![Google ADK](https://img.shields.io/badge/Google_ADK-4285F4?logo=google&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white) ![MCP](https://img.shields.io/badge/Model_Context_Protocol-000000?logo=anthropic&logoColor=white) ![AG-UI](https://img.shields.io/badge/AG--UI-111111) ![Claude](https://img.shields.io/badge/Claude_SDK-D97757?logo=anthropic&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?logo=googlegemini&logoColor=white) ![Gemma](https://img.shields.io/badge/Gemma_4-4285F4?logo=google&logoColor=white) |
| **Evals & safety** | Golden sets · LLM-as-judge with human agreement · CI eval gates · red-teaming · pre-registered experiments · proper scoring rules |
| **Retrieval & data** | Hybrid search (BM25 + vectors) · LanceDB · pgvector · corrective RAG · semantic layers for agents |
| **Models** | PyTorch · YOLO11 segmentation · TimesFM · calibration · scikit-learn |
| **Shipping** | FastAPI · Next.js · Docker · GitHub Actions · DVC · Terraform · OpenTelemetry · GCP (Cloud Run, IAP, Vertex AI, BigQuery) |

---

<p align="center"><i>Building agents that know when <b>not</b> to act is harder than building agents that act.</i></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a7d4a,100:134e4a&height=90&section=footer" width="100%" alt=""/>
