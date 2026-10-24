<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a7d4a,100:134e4a&height=170&section=header&text=Karthick%20Balaje&fontSize=44&fontColor=ffffff&fontAlignY=36&desc=AI%20engineer%20%C2%B7%20LLM%20agents%20that%20are%20evaluated%20before%20they%20ship&descSize=16&descAlignY=58" width="100%" alt="Karthick Balaje, AI engineer"/>

<p align="center">
  <a href="https://linkedin.com/in/karthickbalajege"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://medium.com/@karthickbalaje01"><img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" alt="Medium"/></a>
  <a href="mailto:karthickbalaje01@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Bengaluru,%20India-555555?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Bengaluru, India"/>
</p>

<p align="center"><b>I build LLM agents that are evaluated before they ship and governed once they're live.</b></p>

---

### 🚀 Now

- **In production:** an LLM agent fleet for a US direct-to-consumer apparel brand. It runs 21 scheduled jobs across 10 commerce and marketing APIs, checks every claim against live data before it reaches the founder, and has a person approve every dollar of ad spend.
- **Building:** [Calibrated Health Agent](https://kb2326.github.io/calibrated-health-agent/), a personal health agent that keeps score. It makes daily probabilistic forecasts from my own wearable and journal data and scores them against simple baselines, and every reported number comes with the code that computed it. A public [hash ledger](https://github.com/kb2326/cha-ledger-log) makes the forecast log tamper-evident.

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
- [athlete-ecg-agent](https://github.com/kb2326/athlete-ecg-agent): 12-lead ECG analysis (STAT 5010 project)

</details>

---

### 🧭 How I build

> **Models measure, the agent reasons, rules decide.** Anything with consequences goes through code a person can read.
>
> **Evaluate the evaluator.** An LLM judge is only useful once you've measured how often it agrees with a human.
>
> **Build the outer loop first.** Specs, evals, tracing and approval rules come before the clever part.

---

### 🛠️ Stack

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch,fastapi,react,postgres,docker,githubactions,gcp&perline=8" alt="Python, PyTorch, FastAPI, React, Postgres, Docker, GitHub Actions, GCP"/>
</p>

| | |
|---|---|
| **Agents** | ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white) ![MCP](https://img.shields.io/badge/Model_Context_Protocol-000000?logo=anthropic&logoColor=white) ![Claude](https://img.shields.io/badge/Claude_SDK-D97757?logo=anthropic&logoColor=white) ![Google ADK](https://img.shields.io/badge/Google_ADK-4285F4?logo=google&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?logo=googlegemini&logoColor=white) |
| **Retrieval & evals** | Hybrid search (BM25 + vectors) · LanceDB · pgvector · golden sets · LLM-as-judge · red-teaming |
| **Models** | PyTorch · YOLO11 segmentation · calibration · scikit-learn |
| **Shipping** | FastAPI · Docker · GitHub Actions · DVC · Terraform · GCP |

---

<p align="center"><i>Building agents that know when <b>not</b> to act is harder than building agents that act.</i></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a7d4a,100:134e4a&height=90&section=footer" width="100%" alt=""/>
