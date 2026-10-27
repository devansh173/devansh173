<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:4f46e5&height=170&section=header&text=Devansh%20Bhargava&fontSize=46&fontColor=ffffff&fontAlignY=36&desc=AI%20Engineer%20%E2%80%A2%20Multi-Agent%20Systems%20%E2%80%A2%20Agentic%20RAG&descSize=17&descAlignY=58" width="100%" />

<a href="https://github.com/devansh173">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=3200&pause=900&color=6366F1&center=true&vCenter=true&width=640&lines=Building+production+multi-agent+systems+with+Google+ADK;Agentic+RAG+%E2%80%A2+LangGraph+%E2%80%A2+evals+with+RAGAS+%26+Langfuse;Open-source+contributor+to+Google+ADK%2C+Superset+%26+Agno" alt="Typing intro" />
</a>

<p>
  <a href="https://linkedin.com/in/devansh-bhargava"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:bdevansh173@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://leetcode.com/bdevansh173"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" /></a>
  <img src="https://komarev.com/ghpvc/?username=devansh173&style=for-the-badge&color=4f46e5&label=PROFILE+VIEWS" />
</p>

</div>

---

## 👋 About me

I'm an **AI Engineer** with 1.5 years of experience shipping **production multi-agent and RAG systems** for enterprise clients. I care about the unglamorous parts that make agents usable in the real world: security boundaries, idempotency, evaluation, and observability.

- 🏢 **Junior Software Developer @ [Indium Software](https://www.indiumsoftware.com/)** — building **Data Lifter**, an autonomous Google ADK multi-agent system that migrates databases across engines
- 🧠 Focus areas: **multi-agent orchestration · agentic RAG · LLM evaluation · data platforms (Databricks, Spark)**
- 🌍 Open source: contributions to **Google ADK**, **Apache Superset** and **Agno**
- 🎓 B.Tech CSE (Information Security), **VIT Vellore**
- 🥁 Off the keyboard: classical **tabla** player and **roller skater** 🛼

---

## 🛠️ What I've built at work

<table>
<tr>
<td width="50%" valign="top">

### 🔄 Data Lifter — Indium Software
Autonomous **Google ADK** multi-agent system that migrates databases across engines (e.g. PostgreSQL → Oracle), generating ETL pipelines, views and scripts, and running data ops in flight.

- 🔒 **Zero-data-exposure design**: agents plan and act via metadata and tool calls, so row-level data never reaches the LLM — built for regulated enterprise clients
- ⚡ **3× faster** migrations (5M rows: 90s → 30s) using Google Cloud + Apache Spark as the staging layer

</td>
<td width="50%" valign="top">

### 🧭 Databricks Agent Layer — Indium Software
AI agent layer over **Databricks Unity Catalog** that lets custom Genie-like agents use ontology, business semantics, relationships and governed data for **natural-language analytics and SQL generation**.

### 🏗️ Enterprise Multi-Agent Platform
Agent workflows in **LangGraph** (stateful graphs, conditional routing) and **LangChain** (tool calling, retrieval) on **Azure AI Foundry**, Azure SQL and Cosmos DB.

</td>
</tr>
</table>

<details>
<summary><b>How the zero-data-exposure pattern works</b></summary>
<br>

```mermaid
flowchart LR
    U[User / Migration Request] --> O[Orchestrator Agent]
    O --> P[Planner Agent]
    P -->|schema + stats only| M[(Metadata Catalog)]
    P --> E[Executor Agent]
    E -->|tool calls| T[Migration Tools<br/>ETL · DDL · Views]
    T --> S[(Spark Staging on GCP)]
    S --> D[(Target DB)]
    SRC[(Source DB)] --> S
    classDef llm fill:#4f46e5,color:#fff,stroke:#312e81;
    classDef data fill:#0f172a,color:#fff,stroke:#334155;
    class O,P,E llm;
    class M,S,D,SRC data;
```

The LLM-driven agents (purple) only ever see metadata and tool results. Row-level data moves between the data stores (dark) without passing through a model.

</details>

**Before Indium — Cymake Inc. (Ravan AI):** AI ad/video generation pipeline orchestrating LLMs, diffusion, TTS and lip-sync models over async queues (**70% faster creation, 4× throughput**) · n8n automations integrating 50+ tools with LLM-driven routing (**60% less ops effort**) · RAG pipelines on Pinecone/Weaviate/FAISS · multi-tenant Django microservices with RBAC.

---

## 🚀 Featured projects

<table>
<tr>
<td width="50%" valign="top">

### 📚 [Ask the Docs](https://github.com/devansh173/ask-the-docs)
**Agentic RAG** as a LangGraph state machine: grades retrieval, rewrites and re-searches weak queries, and checks answer groundedness against citations. Works with Claude, Gemini, GPT and Ollama.

| Metric | Naive RAG | Agentic RAG |
|---|:---:|:---:|
| RAGAS faithfulness | 0.885 | **1.0** |
| Answer relevancy | 0.525 | **0.882** |
| Hit@1 (hybrid dense + BM25, RRF) | 0.875 | **1.0** |

`LangGraph` `Qdrant` `FastAPI` `RAGAS` `Langfuse` `Docker`

</td>
<td width="50%" valign="top">

### 🔁 [OraShift](https://github.com/devansh173/orashift)
LLM-powered **Oracle → PostgreSQL SQL translation**, with Oracle Free and Postgres running locally in Docker to validate translated SQL against real engines.

`Python` `LLMs` `Oracle` `PostgreSQL` `Docker`

### 🚗 [Neural Autonomous Driving Simulator](https://github.com/devansh173/neural-autonomous-driving-simulator)
Neural network written **from scratch (no ML frameworks)** that drives a car using 7 ray-cast sensors, trained by a **genetic algorithm** with elitism, crossover and adaptive mutation.

`Python` `NumPy-free NN` `Pygame` `Genetic Algorithms`

</td>
</tr>
</table>

---

## 🌍 Open source contributions

| Project | Contribution | Status |
|---|---|:---:|
| <img src="https://github.com/google.png" width="16"/> **[Google ADK](https://github.com/google/adk-python)** | Fixed Pub/Sub & Eventarc redeliveries re-running agents and repeating tool side effects (e.g. double payments) by exposing delivery IDs as idempotency keys. Backwards compatible, 7 unit tests. [#7325](https://github.com/google/adk-python/pull/7325) | ![](https://img.shields.io/badge/merged-8957e5?style=flat) |
| <img src="https://github.com/google.png" width="16"/> **[ADK Docs](https://github.com/google/adk-docs)** | Documented dead-letter and dedup setup for event-driven agents. [#2274](https://github.com/google/adk-docs/pull/2274) · [#2275](https://github.com/google/adk-docs/pull/2275) | ![](https://img.shields.io/github/pulls/detail/state/google/adk-docs/2275?label=) |
| <img src="https://github.com/apache.png" width="16"/> **[Apache Superset](https://github.com/apache/superset)** | Matched server-side report number formatting to d3-format so negative-zero renders consistently. [#44644](https://github.com/apache/superset/pull/44644) | ![](https://img.shields.io/github/pulls/detail/state/apache/superset/44644?label=) |
| <img src="https://github.com/apache.png" width="16"/> **[Apache Superset](https://github.com/apache/superset)** | Fixed `cast_to_num` crashing on Unicode non-decimal digits. [#44615](https://github.com/apache/superset/pull/44615) | ![](https://img.shields.io/github/pulls/detail/state/apache/superset/44615?label=) |
| <img src="https://github.com/agno-agi.png" width="16"/> **[Agno](https://github.com/agno-agi/agno)** | Preserved MCP audio tool output as agent artifacts, with base64 validation and tests. [#10036](https://github.com/agno-agi/agno/pull/10036) | ![](https://img.shields.io/github/pulls/detail/state/agno-agi/agno/10036?label=) |

<sub>Status badges update automatically from GitHub.</sub>

---

## 🧰 Tech stack

**LLMs & Agents**
<p>
  <img src="https://img.shields.io/badge/Google%20ADK-4285F4?style=flat-square&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/Microsoft%20Agent%20Framework-5E5E5E?style=flat-square" />
  <img src="https://img.shields.io/badge/DSPy-7C3AED?style=flat-square" />
  <img src="https://img.shields.io/badge/MCP-000000?style=flat-square" />
  <img src="https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white" />
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" />
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" />
</p>

**RAG & Evaluation**
<p>
  <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square" />
  <img src="https://img.shields.io/badge/Pinecone-000000?style=flat-square" />
  <img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square" />
  <img src="https://img.shields.io/badge/Hybrid%20Search%20(BM25%20%2B%20Dense)-334155?style=flat-square" />
  <img src="https://img.shields.io/badge/RAGAS-F97316?style=flat-square" />
  <img src="https://img.shields.io/badge/Langfuse-0F172A?style=flat-square" />
</p>

**Data Platforms**
<p>
  <img src="https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/Unity%20Catalog-FF3621?style=flat-square&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
</p>

**Backend & Cloud**
<p>
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,fastapi,django,docker,gcp,azure,aws,postgres,redis,linux,git&perline=11" />
  </a>
</p>

---

## 🏅 Certifications

| | Certification |
|:---:|---|
| 🟠 | **Claude Certified Architect (CCA-F)** — Anthropic |
| 🔴 | **Databricks Certified Generative AI Engineer Associate** |
| 🟡 | **AWS Certified Cloud Practitioner** |

---

## 📊 GitHub activity

<div align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=devansh173&theme=tokyonight&no-frame=true&no-bg=true&margin-w=6&row=1&column=7" />
</div>

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=devansh173&show_icons=true&hide_border=true&bg_color=0d1117&title_color=6366f1&icon_color=6366f1&text_color=c9d1d9&include_all_commits=true&count_private=true" />
  <img height="165" src="https://streak-stats.demolab.com?user=devansh173&hide_border=true&background=0d1117&ring=6366f1&fire=6366f1&currStreakLabel=6366f1&sideLabels=c9d1d9&dates=8b949e&currStreakNum=c9d1d9&sideNums=c9d1d9" />
</div>

---

<div align="center">

**Open to AI Engineer · Forward Deployed Engineer · SDE roles** — let's talk about agents that actually ship. <br/>
<a href="mailto:bdevansh173@gmail.com">bdevansh173@gmail.com</a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4f46e5,100:0f172a&height=100&section=footer" width="100%" />

</div>
