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
<td align="center"><b>10 / 10</b><br/><sub>answers with re-runnable receipts<br/>Health Agent</sub></td>
</tr>
</table>

---

### 🚀 Now

- **In production:** an LLM agent fleet for a US direct-to-consumer apparel brand. It runs 21 scheduled jobs across 10 commerce and marketing APIs, checks every claim against live data before it reaches the founder, and has a person approve every dollar of ad spend.
- **Building in the open soon:** two research projects, both going public once their write-ups are ready (below).

<table>
<tr>
<td width="50%" valign="top">

#### 🫀 Calibrated Health Agent <sub><img src="https://img.shields.io/badge/in_progress-going_public_soon-f2a33a?style=flat-square" alt="In progress, going public soon"/></sub>
A personal health agent on my own wearable and journal data. Ask it a question and it answers with **code it ran in a sandbox**, and every number links to a **receipt you can re-run**. It also tests itself in the strictest way possible: **seven forecasters make sealed, pre-registered daily predictions** that are graded against simple baselines, with the chain of hashes published.

- Google ADK workflow: single agent vs orchestrator + specialists, judged by evals
- Sandboxed code, authorizer-guarded SQL, prompt-injection wrapping, memory
- Nightly investigator files hypotheses that are judged only on later days
- Runs daily on GCP (Cloud Run, Terraform) for **under $1/month**

[Public hash log](https://github.com/kb2326/cha-ledger-log) · [Forecast scoreboard](https://kb2326.github.io/cha-ledger-log/)

`Google ADK` `Gemini` `Vertex AI` `TimesFM` `Terraform` `GCP`

</td>
<td width="50%" valign="top">

#### 🧪 Gemma 4 SWE Agent <sub><img src="https://img.shields.io/badge/in_progress-going_public_soon-f2a33a?style=flat-square" alt="In progress, going public soon"/></sub>
My entry to Kaggle's **Gemma 4 Developer Agent** competition and its **paper track**: *Ask or Enforce? Prompt Rules vs. Agent Structure for a Small Open Model under a Fixed Budget.* A Gemma 4 agent fixes real GitHub issues, graded by hidden tests, within a fixed per-task budget.

- Declarative Google ADK (YAML) agents and prompts, one experiment arm each
- Every prediction committed before its run; held-out tasks fixed by seed
- Paired statistics over transcripts; offline validators for every submission

`Gemma 4` `Google ADK` `Kaggle` `Paired statistics`

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
  <img src="https://skillicons.dev/icons?i=python,pytorch,fastapi,react,postgres,docker,githubactions,gcp&perline=8" alt="Python, PyTorch, FastAPI, React, Postgres, Docker, GitHub Actions, GCP"/>
</p>

| | |
|---|---|
| **Agents** | ![Google ADK](https://img.shields.io/badge/Google_ADK-4285F4?logo=google&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white) ![MCP](https://img.shields.io/badge/Model_Context_Protocol-000000?logo=anthropic&logoColor=white) ![Claude](https://img.shields.io/badge/Claude_SDK-D97757?logo=anthropic&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?logo=googlegemini&logoColor=white) ![Gemma](https://img.shields.io/badge/Gemma_4-4285F4?logo=google&logoColor=white) |
| **Evals & safety** | Golden sets · LLM-as-judge with human agreement · red-teaming · pre-registered experiments · proper scoring rules |
| **Retrieval** | Hybrid search (BM25 + vectors) · LanceDB · pgvector · corrective RAG |
| **Models** | PyTorch · YOLO11 segmentation · TimesFM · calibration · scikit-learn |
| **Shipping** | FastAPI · Docker · GitHub Actions · DVC · Terraform · GCP (Cloud Run, Vertex AI, BigQuery) |

---

<p align="center"><i>Building agents that know when <b>not</b> to act is harder than building agents that act.</i></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a7d4a,100:134e4a&height=90&section=footer" width="100%" alt=""/>
