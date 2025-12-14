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
-
  # Simulating Fine-Tuning Behavior (Without Fine-Tuning)

This notebook demonstrates **what fine-tuning actually changes** by simulating
a fine-tuned model using:
- Structured examples
- Behavioral conditioning
- Strict output enforcement

No real fine-tuning.
No training cost.
No hallucinated promises.

Goal: understand *when* fine-tuning is worth it.


### Hands-On Activities
- Build a Meeting Scheduler Bot & A RAG Agent   
  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sMJtqFFVbJoYCQPqVJef6zFmRWWgMc7f#scrollTo=X8yP76TBodHA)
- Multiagent Content Crew [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1frj1fTXRtmCsML4N_pfGpykwpHr7ToGV)
-RL Hands-on [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZYDwduZjvc51o_2MTdOQTKaB68SqpJ_H)
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

```text
Schedule Trigger
↓
Set (date_utc, raw_inputs)
↓
IF (skip empty input)
├─ TRUE  → OpenAI → Parse JSON → Format Email → Gmail Send
└─ FALSE → Optional “No Updates” Email / NoOp
```
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
### Prompt
```text
You are an expert AI engineer and Python/Streamlit developer.
Your task is to generate a **complete, production-ready AI application** using 
**Streamlit + OpenAI API**, fully deployable on **Render**.

This application must use the **P.E.A.C.E. Prompt Framework** for all LLM interactions:
P — Purpose  
E — Expectations  
A — Actions  
C — Constraints  
E — Evaluation  

Whenever you create an LLM prompt, structure it explicitly using these five sections.

=====================================================
APP — Agentic AI Data Analysis Bot (Render-ready)
=====================================================

FEATURES (must include all of the following):
- CSV uploader
- Dataset preview (df.head(), df.info())
- Rich dataset summary extracted via pandas
- Agentic workflow using OpenAI that generates:
    - Data cleaning strategy
    - Feature engineering suggestions
    - ML model selection (classification/regression)
    - Python code for training (using pandas + scikit-learn + matplotlib)
    - Evaluation metric explanation
- Full report displayed in Streamlit
- Option to download the report (e.g., as .txt)

=====================================================
LLM PROMPT REQUIREMENTS (use PEACE Framework)
=====================================================

For the main LLM call that analyzes the dataset, build the prompt using the PEACE structure:

P — Purpose:  
    The agent will analyze the dataset in detail as a senior data scientist.

E — Expectations:  
    Provide a complete analytical pipeline including:
    - Data cleaning steps
    - Feature engineering strategy
    - Model selection rationale (and whether the task is regression or classification)
    - Python code for the entire ML pipeline
    - Explanation of evaluation metrics and how to interpret them

A — Actions:  
    Examine dataset summary → reason about transformations → propose the best model(s) →  
    generate Python code → explain results in clear, academic language.

C — Constraints:  
    - No hallucinated columns or features  
    - Only use columns provided in the dataset  
    - Avoid incorrect assumptions (state assumptions explicitly if needed)  
    - If unsure about task type (regression vs classification), clearly state the assumption  
    - Do not fabricate metric values; only provide code to compute them

E — Evaluation:  
    Ensure the output is:
    - Correct and logically consistent  
    - Structured with sections (e.g., Cleaning, Features, Model, Code, Evaluation)  
    - Reproducible by a graduate student using Python  

You must implement this PEACE prompt explicitly as a string in the code and pass it to the OpenAI API.

=====================================================
SHARED CODING REQUIREMENTS
=====================================================

Generate:

1. A full `app.py` file that:
   - Uses **Streamlit** for the UI
   - Uses the **OpenAI Python SDK** with this pattern:
         from openai import OpenAI
         client = OpenAI(api_key=st.secrets["OPENAI_API_KEY"])
   - Loads the API key from `st.secrets["OPENAI_API_KEY"]` (Render-compatible)
   - Includes basic error handling (e.g., missing key, API failures)
   - Has clear comments explaining:
       - UI components
       - LLM call
       - PEACE prompt construction
   - Runs without modification when deployed on Render

2. A `requirements.txt` file containing exactly:
   streamlit  
   openai  
   pandas  
   matplotlib  

3. A **Render Deployment Guide** that includes:
   - Build command:
         pip install -r requirements.txt
   - Start command:
         streamlit run app.py --server.port $PORT --server.address 0.0.0.0
   - Instruction to set `OPENAI_API_KEY` in Render’s Environment variables

=====================================================
FINAL OUTPUT FORMAT
=====================================================

Return your answer exactly in this structure:

### 1. Application — Agentic AI Data Analysis Bot

#### app.py
```python
# full code here
```


## 📚 Application 2 — Literature Review & Paper Summarizer
Features:

- PDF ingestion  
- Summary + gap analysis  
- BibTeX extraction  
- Mini-survey creation  
- RAG-based semantic search  
- Export to LaTeX
### Prompt
```text
You are an expert AI engineer and Python/Streamlit developer.
Your task is to generate a **complete, production-ready AI application** using 
**Streamlit + OpenAI API**, fully deployable on **Render**.

This application must use the **P.E.A.C.E. Prompt Framework** for all LLM interactions:
P — Purpose  
E — Expectations  
A — Actions  
C — Constraints  
E — Evaluation  

Whenever you create an LLM prompt, structure it explicitly using these five sections.

=====================================================
APP — AI Research Assistant (Render-ready)
=====================================================

FEATURES (must include all of the following):
- Text input for research topic (or abstract)
- Optional input for field/discipline (e.g., Materials Science, CS, Education)
- Uses LLM to generate:
    - A concise academic **Summary**
    - A list of **Research gaps**
    - **Methodology suggestions**
    - A **Related work overview**
    - Example **APA-style references**
- Structured outputs with clear headings
- Clean Streamlit layout
- Option to download the generated overview as Markdown

=====================================================
LLM PROMPT REQUIREMENTS (use PEACE Framework)
=====================================================

For the core LLM call that acts as the research assistant, build the prompt using PEACE:

P — Purpose:  
    Assist the researcher by generating a structured academic overview of the given topic.

E — Expectations:  
    Provide concise but detailed academic sections with:
    - A 150–250 word summary
    - 3–6 research gaps
    - 3–5 methodology suggestions
    - A short related work overview
    - 5–8 example APA-style references

A — Actions:  
    - Summarize the topic  
    - Identify important gaps and open questions  
    - Propose methodologies (experimental, computational, theoretical, mixed)  
    - Outline related work themes  
    - Provide realistic but not fabricated APA-style references

C — Constraints:  
    - Avoid confidently fabricated citations (titles/authors/years)  
    - It’s acceptable to provide **generic** / **approximate** references, but label them as examples if needed  
    - Use real methods and terminology appropriate to the field  
    - If there is insufficient information, say “insufficient data” or state assumptions clearly  
    - Maintain an academic tone and structure

E — Evaluation:  
    Output must:
    - Follow an academic tone  
    - Use headings for each section:
      - Summary
      - Research Gaps
      - Methodology Suggestions
      - Related Work Overview
      - Example References (APA)  
    - Be logically coherent and helpful to a graduate student or early-stage researcher  

You must implement this PEACE prompt explicitly as a string in the code and pass it to the OpenAI API.

=====================================================
SHARED CODING REQUIREMENTS
=====================================================

Generate:

1. A full `app.py` file that:
   - Uses **Streamlit** for UI
   - Uses the **OpenAI Python SDK** with this pattern:
         from openai import OpenAI
         client = OpenAI(api_key=st.secrets["OPENAI_API_KEY"])
   - Loads the API key from `st.secrets["OPENAI_API_KEY"]` (Render-compatible)
   - Includes basic error handling (e.g., missing key, API failure)
   - Has clear comments explaining:
       - UI fields
       - LLM call
       - PEACE prompt construction
   - Provides a **Download as Markdown** button for the generated overview
   - Runs without modification when deployed on Render

2. A `requirements.txt` file containing exactly:
   streamlit  
   openai  
   pandas  
   matplotlib  

   (Even if not all are used, keep it identical to the other app for simplicity.)

3. A **Render Deployment Guide** that includes:
   - Build command:
         pip install -r requirements.txt
   - Start command:
         streamlit run app.py --server.port $PORT --server.address 0.0.0.0
   - Instruction to set `OPENAI_API_KEY` in Render’s Environment variables

=====================================================
FINAL OUTPUT FORMAT
=====================================================

Return your answer exactly in this structure:

### 1. Application — AI Research Assistant

#### app.py
```python
# full code here
```
