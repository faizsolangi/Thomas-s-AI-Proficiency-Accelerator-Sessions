# AI Proficiency Accelerator — 4-Session Training  
### Build Real Agentic AI Skills in 6 Hours  


---

## 🚀 Training Overview

This 4-session, 6-hour applied training equips participant, production-ready skills in:

- Git & reproducible AI workflows  
- Advanced prompt engineering (CoT, self-consistency, tool-calling)  
- Custom GPT development for engineering tasks  
- GenAI & Agentic AI foundations  
- RAG pipelines using Pinecone  
- No-code automation with n8n  
- Rapid agent prototyping using CrewAI  
- Deploying Streamlit apps to Render  
- Building internal engineering AI tools  

Each session is **1.5 hours**, hands-on, and optimized for a **mission-critical engineering environment**.

---

# 🔥 Session Breakdown

---

# 🧩 Session 1 — Git + Google Colab + Prompt Engineering + Custom GPT (1.5 hrs)

### Topics Covered
- Git & GitHub workflow for AI engineering  
- Google Colab as a reproducible AI dev environment  
- Structured prompt engineering (zero-shot, few-shot, CoT, SC, tool-calling)  
- Building a Custom GPT for engineering workflows  
- Organizing AI repos for reliability & traceability  

### Hands-On Activities 
- Run your first LLM API call in Colab  
- Build high quality prompts (requirements review, log summaries, code review)
-  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1BihIWRJdskAXWuYQaT9zkBZMAgnYWxe2#scrollTo=uMrCuVwfYRrj)
- Create a “Custom GPT”  

### Key Outcomes
Thomas learns professional AI dev workflows, gains a prompt engineering toolkit, and builds first internal-use Custom GPT.

---

# 🧠 Session 2 — GenAI Concepts + Agentic AI + RAG with Pinecone (1.5 hrs)

### Topics Covered
- How LLMs work (engineer-friendly explanation)  
- Prompting vs fine-tuning vs embeddings vs RAG  
- Agentic AI fundamentals  
- ReAct logic (reason → act → observe → reflect)   
- ChromaDB RAG pipeline (chunking, embedding, querying)  

### Hands-On Activities
- Build a Meeting Scheduler Bot & A RAG Agent   
  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sMJtqFFVbJoYCQPqVJef6zFmRWWgMc7f#scrollTo=X8yP76TBodHA)
- Multiagent Content Crew [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1frj1fTXRtmCsML4N_pfGpykwpHr7ToGV)

### Key Outcomes
Thomas builds a working RAG pipeline and understands the architecture behind LLM-powered knowledge systems.

---

# ⚙️ Session 3 — No-Code Automation (n8n) + Daily Briefing Workflow (1.5 hrs)

### Topics Covered
- No-code automation principles  
- Designing production-ready workflows  
- LLM → n8n integrations  
- Using triggers, gmail, API calls  
- Multi-source data ingestion (email, tasks, logs)  

### Hands-On Project  
### n8n + OpenAI + Gmail

This repository contains the **complete, end-to-end implementation** of the **Daily Engineering Briefing** built during **Session 3** of the *AI Proficiency Accelerator*.

The purpose of this session is to demonstrate how **Large Language Models (LLMs)** move from **isolated prompts** to **reliable, automated, production-grade systems** using **n8n**, with **secure credential handling** and **engineering-grade workflow design**.

Everything required to understand, reproduce, and extend this system is documented below.

---

## 🎯 What This System Does

On a daily schedule, the workflow:

1. Collects engineering inputs  
2. Uses an LLM to generate a **structured engineering briefing**  
3. Formats the output into a human-readable report  
4. Sends the briefing via **Gmail**

Each briefing contains:
- Key events  
- Anomalies  
- Recommended actions  
- Risk level  
- Notes / assumptions  
- raw_inputs
[02:14:08 UTC] Attitude control subsystem switched to Safe Mode due to unexpected torque spike on Reaction Wheel #3.
[02:14:12 UTC] Telemetry indicates wheel speed exceeded nominal range by +18%. Automatic braking applied.
[02:14:17 UTC] Thermal sensors in Bay 2 reported a sudden 6°C rise over 20 seconds, triggering thermal warning flag (TW-04).
[02:14:25 UTC] Command uplink lost for 4 seconds during Safe Mode transition. Link restored automatically.
[02:14:32 UTC] System performed health diagnostics: no structural damage detected; Reaction Wheel #3 flagged for recalibration.
[02:15:10 UTC] Power subsystem switched from Battery Pack B to Pack A due to voltage fluctuation (−0.9 V below threshold).


---

## 🧱 Workflow Architecture (Logical Flow)


Schedule Trigger
↓
Set (date_utc, raw_inputs)
↓
IF (skip empty input)
├─ TRUE  → OpenAI → Parse JSON → Format Email → Gmail Send
└─ FALSE → Optional “No Updates” Email / NoOp

**Workflow Template:**  
`/automation/n8n_daily_briefing.json`

### Key Outcomes
Learns to automate engineering workflows and connect LLM outputs to real-time systems.


# 📈 Session 4 — Applications: Academic AI Tools (1.5 hrs)

### Topics Covered
- Principles of fast AI prototyping  
- Designing small academic AI apps  
- Streamlit front-end for AI  
- Connecting Python backend + OpenAI API  
- Deploying on Render  


## 🧪 Application 1 — Agentic AI Data Analysis Bot
A Streamlit-based automated data analysis assistant that performs:

- Data cleaning  
- Feature engineering  
- AutoML model selection  
- Model training & evaluation  
- Dashboard visualization  
- Exportable reports  
- Deployable on Render  

Perfect for graduate research & faculty projects.

---

## 📚 Application 2 — Literature Review & Paper Summarizer
Features:

- PDF ingestion  
- Summary + gap analysis  
- BibTeX extraction  
- Mini-survey creation  
- RAG-based semantic search  
- Export to LaTeX  

Ideal for research groups, PhD students, and grant proposals.
