# 🧠 Advanced RAG (Retrieval-Augmented Generation)

A modular, end-to-end hands-on repository covering advanced architectures, techniques, and optimizations for production-grade **Retrieval-Augmented Generation (RAG)** systems using LangChain, vector stores, rerankers, and modern LLMs.

---

## 🏗️ Repository Architecture

The repository is organized into distinct, self-contained modules following each step in an advanced RAG lifecycle:

```text
advance-rag/
├── RAG-DOCUMENT-LOADER/             # Module 1: Multi-format Ingestion & Document Parsing
│   ├── knowledge-source/            # Sample documents (PDF, CSV, TXT, JSON)
│   ├── notebooks/                   # Hands-on Jupyter notebooks
│   │   ├── csv_loader.ipynb         # CSVLoader for tabular records
│   │   ├── pdf_loader.ipynb         # PyPDF, RapidOCR, PDFMiner, PDFPlumber
│   │   └── text_loader.ipynb        # TextLoader with metadata extraction
│   ├── requirements.txt             # Module dependencies
│   └── README.md                    # Detailed loader documentation
│
├── RAG-TEXT-SPLITTER/               # Module 2: Text Chunking Strategies (Upcoming)
│   └── README.md                    # Recursive, token, markdown, and semantic chunking
│
├── .gitignore                       # Clean Git tracking (ignores .venv, caches, etc.)
└── README.md                        # Master project documentation
```

---

## 🗺️ Learning Roadmap

| # | Stage / Module | Status | Description |
|---|---|:---:|---|
| **01** | [**RAG-DOCUMENT-LOADER**](./RAG-DOCUMENT-LOADER/) | ✅ Available | Ingestion for PDF (digital & OCR), CSV, plain text, and JSON with metadata tracking. |
| **02** | [**RAG-TEXT-SPLITTER**](./RAG-TEXT-SPLITTER/) | ⏳ Upcoming | Recursive, character, token-based, Markdown-aware, and semantic chunking strategies. |
| **03** | **RAG-EMBEDDINGS-VECTORDB** | 📋 Planned | Dense & sparse embeddings, FAISS, ChromaDB, and Pinecone vector indexing. |
| **04** | **RAG-RETRIEVAL-RERANKING** | 📋 Planned | Hybrid search (BM25 + Dense vector), Cross-Encoders, Cohere Rerank, and Multi-Query. |
| **05** | **ADVANCED-EVAL-AGENTIC** | 📋 Planned | RAG Triad evaluation (Ragas/TruLens), Self-RAG, Corrective RAG (CRAG), and Agentic routing. |

---

## ⚡ Quickstart Guide

### 1. Clone the Repository
```bash
git clone https://github.com/singhanuj1393/advance-rag.git
cd advance-rag
```

### 2. Set Up Virtual Environment
```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install Dependencies
```bash
cd RAG-DOCUMENT-LOADER
pip install -r requirements.txt
```

### 4. Run Notebooks
```bash
jupyter notebook notebooks/
```

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
