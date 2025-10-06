# finwise-genai-capstone

## 🚀 Overview

This project implements an **End-to-End Natural Language to SQL Question Answering (SQL-QA) system**.
It allows users to ask questions in **plain English**, automatically converts them into **SQL queries**, executes on a **SQLite database**, and returns results.

**My Contribution:** I worked on Task-05 and Task-06, where I built the SQL-QA system, database setup, backend (FastAPI), and frontend (Streamlit) for natural language to SQL execution.

The project is divided into two parts:

* **Task-05:** Basic SQL-QA pipeline using FastAPI + LangChain + SQLite.
* **Task-06:** Extended SQL-QA with a Streamlit frontend, improved schema, and query execution.

---

## 📂 Project Structure

```
finwise-genai-capstone/
├── task-05-sql-qa/
│   ├── create_db.py          # Creates portfolio.db with sample data
│   ├── sql_qa_system.py      # FastAPI backend (Task-05)
│   ├── streamlit_app.py      # Streamlit frontend
│   ├── requirements.txt      # Dependencies
│   └── portfolio.db          # Auto-created database
│
├── task-06-sql-qa-advanced/
│   ├── create_db.py          # Advanced schema + sample data
│   ├── sql_qa_system.py      # FastAPI backend (Task-06)
│   ├── streamlit_app.py      # Streamlit UI with results
│   ├── requirements.txt      # Dependencies
│   └── portfolio.db          # Auto-created database
│
└── README.md                 # Project documentation
```

---

## ⚡ Features

✅ **Task-05**

* Natural language to SQL query generation.
* FastAPI backend (`/query` endpoint).
* SQLite database with sample campaigns & transactions.

✅ **Task-06**

* Enhanced schema with campaigns + transactions.
* Improved SQL generation with LangChain + Gemini.
* Streamlit frontend for easy interaction.
* Display SQL + results in table format.

---

## 🛠️ Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/<your-username>/sql-qa-system.git
cd sql-qa-system
```

### 2. Create Virtual Environment

```bash
python -m venv .venv
.\.venv\Scripts\activate     # Windows
source .venv/bin/activate    # Mac/Linux
```

### 3. Install Dependencies

```bash
pip install -r task-05-sql-qa/requirements.txt
pip install -r task-06-sql-qa-advanced/requirements.txt
```

### 4. Set API Key

Export your Google Gemini API key:

```bash
set GOOGLE_API_KEY=your_api_key_here    # Windows
export GOOGLE_API_KEY=your_api_key_here # Mac/Linux
```

---

## ▶️ Run the Projects

### Task-05

1. Create DB:

   ```bash
   cd task-05-sql-qa
   python create_db.py
   ```
2. Start backend:

   ```bash
   python -m uvicorn sql_qa_system:app --reload --port 8000
   ```

   Open: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
3. Run Streamlit UI:

   ```bash
   streamlit run streamlit_app.py
   ```

   Open: [http://localhost:8501](http://localhost:8501)

---

### Task-06

1. Create DB:

   ```bash
   cd task-06-sql-qa-advanced
   python create_db.py
   ```
2. Start backend:

   ```bash
   python -m uvicorn sql_qa_system:app --reload --port 8000
   ```
3. Run Streamlit UI:

   ```bash
   streamlit run streamlit_app.py
   ```

---

## 📝 Example Queries

* *“List top 5 campaigns by ROI in the last 6 months.”*
* *“Show total spend per campaign.”*
* *“Find all transactions greater than 500.”*
* *“Which campaign generated the highest revenue?”*

---

## 📊 Tech Stack

* **Backend:** FastAPI, Uvicorn
* **Frontend:** Streamlit
* **Database:** SQLite
* **LLM:** Google Gemini via LangChain

---

## 🔮 Future Improvements

* Add authentication & role-based access.
* Add error-handling for invalid SQL.
* Visualize results as charts in Streamlit.
* Extend DB with more real-world financial data.

---

## 👨‍💻 Author

**Dhruv Mehta**
Capstone Project – AI / Data Science
**My contribution in this project: Task-05 and Task-06 (SQL-QA System + Summarization).**


