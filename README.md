# 🚀 Finwise GenAI Capstone – MarketGen Solutions

**MarketGen Solutions** is a digital marketing & customer analytics firm that is rapidly adopting **GenAI** to compete with rivals like BrandNext.  
This project is an **end-to-end prototype** of AI-powered marketing assistants, built in just **7 days** by a 3-member AI Engineering team.  

---

## 📖 Project Overview
We extended the **MedAssist IQ Platform** with GenAI capabilities to handle:
- Customer persona creation  
- Campaign optimization  
- Real-time personalization  
- Automated reporting & insights  

This repo includes **Task 1–8** (except Task 7, which is optional).

---

## ⚡ Tech Stack
- **LLM Backbone**: Google Gemini Pro (via Google AI Studio API)  
- **Frameworks**: LangChain, LangGraph  
- **Databases**: SQLite, FAISS  
- **Automation**: n8n  
- **APIs & Tools**: FastAPI, Uvicorn, DuckDuckGoSearch, Python REPL  
- **Development**:  
  - Google Colab → Task 1, 2, 3, 4, 8  
  - VS Code → Task 5 (SQL QA), Task 6 (Summarization)  

---

## 📂 Repository Structure
```

📁 finwise-genai-capstone/
├── 📁 task-01-chatbot-memory/      # Colab
├── 📁 task-02-agent-tools-langgraph/  # Colab
├── 📁 task-03-rag-basic/           # Colab
├── 📁 task-04-rag-advanced-memory/ # Colab
├── 📁 task-05-sql-qa/              # VS Code
├── 📁 task-06-summarization/       # VS Code
├── 📁 task-08-workflow-automation-n8n/ # Colab
├── 📄 README.md (this file)
└── requirements.txt

```

---

## 📝 Tasks Breakdown

### ✅ Task 1 – Marketing Chatbot with Memory *(Colab)*
- Chatbot with memory for marketers & clients.  
- Built using **LangChain + Gemini** with ConversationBufferMemory.  

---

### ✅ Task 2 – AI Agent with External Tool Access *(Colab)*
- AI Agent that segments customers, forecasts ROI, and predicts churn.  
- Powered by **LangGraph + LangChain Tools** (DuckDuckGoSearch, Python REPL).  

---

### ✅ Task 3 – RAG (Document QA) *(Colab)*
- Query PDFs like brand manuals & campaign briefs.  
- Uses **FAISS, LangChain, RetrievalQA, VertexAI Embeddings**.  

---

### ✅ Task 4 – Advanced RAG with Memory *(Colab)*
- Enhanced RAG with **multi-step retrieval + memory**.  
- Supports context-aware campaign comparison.  

---

### ✅ Task 5 – SQL QA System *(VS Code)*
- Query structured marketing datasets via **natural language**.  
- Uses **SQLite, LangChain SQLDatabaseChain, FastAPI**.  
- Example:  
```

User: List top 5 campaigns by ROI in last 6 months.
Bot: Generates SQL → Executes → Returns table + summary.

````

---

### ✅ Task 6 – Summarization Engine *(VS Code)*
- Summarize **surveys, NPS feedback, campaign analytics**.  
- Uses **LangChain Summarization Chains (MapReduce, Refine)**.  

---

### ✅ Task 8 – Workflow Automation *(Colab)*
- Workflow automation using **n8n**.  
- Alerts, logging, notifications integrated with marketing workflows.
  
![task-08-my-workflow](https://github.com/user-attachments/assets/130551cb-1d89-4da1-ab0c-1afe76cb19e0)

---

## 🚀 Setup & Run

### 1. Clone Repo
```bash
git clone https://github.com/<your-username>/finwise-genai-capstone.git
cd finwise-genai-capstone
````

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Run in Colab

* Open `task-01` to `task-04`, and `task-08` notebooks in Google Colab.
* Execute cells step by step.

### 4. Run in VS Code

#### Task 5 (SQL QA)

```bash
cd task-05-sql-qa
python create_db.py
uvicorn sql_qa_system:app --reload --port 8000
```

Test:

```bash
curl -X POST "http://localhost:8000/query" \
  -H "Content-Type: application/json" \
  -d '{"query": "List top 5 campaigns by ROI"}'
```

#### Task 6 (Summarizer)

```bash
cd task-06-summarization
python summarizer.py
```

---

## 👥 Project Note

This is **our group project** built collaboratively as part of the Finwise GenAI Capstone.

---
