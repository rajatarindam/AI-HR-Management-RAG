# 🤖 Enterprise HR Intelligence Assistant (RAG-Based)

## 🚀 Overview

This project is an **AI-powered HR Management Assistant** built using **Retrieval-Augmented Generation (RAG)**.

It helps employees, managers, and HR teams get **accurate, company-specific answers** to HR-related queries such as:

* Leave policies
* Promotion eligibility
* Salary structure
* Probation rules
* Interview process
* Reimbursement policies

Unlike generic chatbots, this system retrieves answers directly from **internal HR policy documents**, ensuring **accuracy, reliability, and zero hallucination**.

---

## 🎯 Key Features

* 📄 **HR Policy Q&A using RAG**
* 🔍 **Semantic Search with pgvector (Supabase)**
* ⚡ **FastAPI Backend for real-time responses**
* 🧠 **NVIDIA Embeddings for high-quality retrieval**
* 🛡️ **Intent-aware fallback system for low-confidence queries**
* 🧩 **Hybrid system: RAG + structured database logic**

---

## 🧠 How It Works

```text
User Query
   ↓
Query Embedding (NVIDIA)
   ↓
Vector Search (pgvector)
   ↓
Top Relevant HR Chunks Retrieved
   ↓
Confidence Check
   ↓
(RAG Engine OR Fallback Engine)
   ↓
LLM Response Generation
   ↓
Final Answer
```

---

## 🏗️ Tech Stack

* **Backend:** FastAPI
* **Database:** Supabase PostgreSQL + pgvector
* **Embeddings:** NVIDIA NIM API
* **Language:** Python
* **Architecture:** RAG + Fallback Hybrid

---

## 📂 Project Structure

```
.
├── legal_corpus/          # HR policy documents (RAG knowledge base)
├── fallback_data/         # Fallback corpus for reliability
├── store_chunks.py        # Document ingestion + embedding
├── retriever.py           # Vector search logic
├── fallback_engine.py     # Fallback decision system
├── trigger_engine.py      # Query routing logic
├── embeddings.py          # NVIDIA embedding integration
├── text_chunker.py        # Chunking logic
├── main.py                # Test entry point
├── .env.example           # Environment template
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone Repo

```bash
git clone https://github.com/YOUR_USERNAME/AI-HR-Management-RAG.git
cd AI-HR-Management-RAG
```

### 2. Setup Environment

Create `.env` using `.env.example`

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Ingest Documents

```bash
python store_chunks.py
```

### 5. Run System

```bash
python main.py
```

---

## 🧪 Example Queries

Try asking:

* How many casual leaves are allowed and can they be carried forward?
* Can probation be extended and under what conditions?
* Who is eligible for promotion?
* What are common reasons for promotion delays?
* What is the interview process?

---

## 🧠 Why This Project Stands Out

* ❌ No generic chatbot answers
* ✅ Uses real HR policy documents
* ✅ Hybrid system (RAG + fallback)
* ✅ Handles real-world messy queries
* ✅ Designed for enterprise internal use

---

## 🔐 Security Note

* No API keys or sensitive data included
* Uses `.env` for configuration
* Synthetic HR dataset used (no confidential data)

---

## 📌 Future Improvements

* Frontend chat interface (React)
* Role-based HR access control
* Real-time HR dashboard
* Multi-domain RAG support
* Advanced semantic chunking

---

## 👨‍💻 Author
GitHub: https://github.com/rajatarindam
