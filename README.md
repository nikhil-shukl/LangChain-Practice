🚀 Generative AI & RAG with LangChain 1.x

This repository contains end-to-end implementations of Generative AI and Retrieval-Augmented Generation (RAG) systems built using LangChain 1.x, following modern runnable-based pipelines instead of deprecated chain abstractions.

The project demonstrates the complete workflow — from data ingestion to vector storage, retrieval, and context-aware LLM generation, using both OpenAI and open-source models (Ollama, HuggingFace).

🧠 Key Concepts Covered

LangChain 1.x runnable pipelines (no deprecated chains)

Retrieval-Augmented Generation (RAG)

Context-aware LLM responses

Vector similarity search

Production-style modular design

🛠️ Tech Stack

LangChain 1.x

OpenAI (GPT-4 / GPT-4o-mini)

Ollama (local LLMs & embeddings)

FAISS & ChromaDB (Vector Stores)

HuggingFace Embeddings

Python

Streamlit (Chat UI)

LangSmith (Tracing & Observability)

📂 Project Structure
llm_projects/
│
├── 1-openai/
│   ├── Getting started with LangChain & OpenAI
│   └── Simple GenAI / RAG apps
│
├── 2-ollama/
│   ├── Local LLM usage with Ollama
│
├── 3-DataIngestion/
│   ├── Web, text, JSON, Arxiv loaders
│
├── 4-Embeddings/
│   ├── OpenAI embeddings
│   ├── Ollama embeddings
│   └── HuggingFace embeddings
│
├── 5-VectorStore/
│   ├── FAISS
│   ├── ChromaDB
│   └── Similarity search & retrievers
│
├── Streamlit Chat App
│
├── .env
├── requirements.txt
└── README.md

🔁 RAG Architecture (LangChain 1.x)
User Query
   ↓
Retriever (FAISS / Chroma)
   ↓
Relevant Documents
   ↓
Prompt Template
   ↓
LLM (OpenAI / Ollama)
   ↓
StrOutputParser
   ↓
Final Answer

✨ Highlights

✅ Migrated from deprecated chains to pure runnable pipelines

✅ Explicit retrieval and context injection (no black-box logic)

✅ Supports both cloud and local LLMs

✅ Clean, debuggable, production-ready architecture

✅ Streamlit-based chatbot interface

🧪 Example: Runnable-based RAG (LangChain 1.x)
docs = retriever.invoke(question)
context = "\n".join([doc.page_content for doc in docs])

answer = rag_pipeline.invoke({
    "context": context,
    "question": question
})

🚀 Getting Started

Clone the repository

Create a virtual environment

Install dependencies:

pip install -r requirements.txt


Add your API keys in .env

Run notebooks or Streamlit app

🎯 Learning Outcome

This repository is ideal for:

Developers learning modern LangChain 1.x

Understanding real-world RAG pipelines

Building production-grade GenAI applications

📌 Author

Nikhil Shukla
Generative AI | LangChain | RAG | LLM Engineering
