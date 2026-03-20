# 🧠 Medical AI Assistant (RAG-Based)

🚀 **Live Demo (Frontend):**
👉 https://medicalaiassistant2.streamlit.app/

---

## 📌 Overview

Medical AI Assistant is a **Retrieval-Augmented Generation (RAG)** based system that allows users to upload medical documents (PDFs) and ask questions based on their content.

The system processes documents into embeddings, stores them in a vector database, and retrieves relevant information to generate accurate, context-aware responses using a Large Language Model (LLM).

---

## ⚙️ Architecture

```
User (Streamlit UI)
        ↓
FastAPI Backend (Render)
        ↓
Embedding Model (HuggingFace)
        ↓
Vector Database (Pinecone)
        ↓
Retriever → LLM (Groq)
        ↓
Context-aware Answer
```

---

## 🔥 Features

* 📄 Upload and process medical PDFs
* 🔍 Semantic search using vector embeddings
* 🤖 Context-aware answers using LLM (Groq)
* ⚡ Fast retrieval with Pinecone vector database
* 🌐 Full-stack deployment (Streamlit + Render)
* 🧩 Modular backend architecture (FastAPI)
* 📊 Source-aware responses (retrieved documents)

---

## 🧠 How It Works (RAG Pipeline)

1. **Document Upload**

   * PDFs are uploaded via frontend
   * Stored and processed in backend

2. **Text Processing**

   * Extract text using PDF loader
   * Split into smaller chunks

3. **Embedding Generation**

   * Convert text → vector embeddings (HuggingFace)

4. **Vector Storage**

   * Store embeddings in Pinecone

5. **Query Handling**

   * User question → embedding
   * Retrieve top-k relevant chunks

6. **LLM Generation**

   * Pass context + query to LLM (Groq)
   * Generate grounded response

---

## 🏗️ Project Structure

```
MedicalAiAssistant/
│
├── client/                  # Streamlit frontend
│   ├── components/
│   ├── utils/
│   └── app.py
│
├── server/                  # FastAPI backend
│   ├── routes/              # API endpoints
│   ├── modules/             # Core RAG logic
│   ├── middlewares/
│   └── main.py
│
├── uploaded_docs/           # Uploaded PDFs
└── requirements.txt
```

---

## 🚀 Tech Stack

### 🔹 Backend

* FastAPI
* LangChain
* Pinecone (Vector DB)
* Groq (LLM)
* HuggingFace Embeddings

### 🔹 Frontend

* Streamlit

### 🔹 Deployment

* Render (Backend)
* Streamlit Cloud (Frontend)

---

## 🛠️ Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/MedicalAiAssistant.git
cd MedicalAiAssistant
```

---

### 2️⃣ Create Virtual Environment

```bash
python -m venv .venv
.venv\Scripts\activate   # Windows
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r server/requirements.txt
pip install -r client/requirements.txt
```

---

### 4️⃣ Setup Environment Variables

Create `.env` file:

```env
PINECONE_API_KEY=your_key
PINECONE_INDEX_NAME=medicalindex-hf
GROQ_API_KEY=your_key
```

---

### 5️⃣ Run Backend

```bash
uvicorn server.main:app --reload
```

---

### 6️⃣ Run Frontend

```bash
streamlit run client/app.py
```

---

## 🌐 Deployment

* **Backend:** Deployed on Render
* **Frontend:** Deployed on Streamlit Cloud

---

## 📈 Future Improvements

* 🔁 Conversational memory (chat history)
* 🔍 Hybrid search (BM25 + vector)
* 🧠 Re-ranking for better accuracy
* ⚡ Streaming responses
* 🔐 Authentication & user sessions
* ☁️ Scalable async processing (Celery/Redis)

---

## 🎯 Interview Highlights

* Implemented end-to-end **RAG pipeline**
* Used **vector databases for semantic retrieval**
* Integrated **LLM with context grounding**
* Designed **modular and scalable backend architecture**
* Deployed full-stack AI system in production

---

## 🙌 Acknowledgements

* LangChain
* Pinecone
* Groq
* HuggingFace

---

## 📬 Contact

If you found this useful, feel free to connect! 🚀
