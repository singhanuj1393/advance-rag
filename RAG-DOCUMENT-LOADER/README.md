# RAG Document Loader

The **Document Ingestion** stage is the foundation of any Retrieval-Augmented Generation (RAG) system. Real-world enterprise data exists across diverse formats—PDFs with scanned pages and diagrams, CSV tables, plain text, and nested JSON.

This module provides comprehensive, hands-on implementations for ingesting, parsing, and extracting metadata across multiple data formats using LangChain community loaders.

---

## 📂 Directory Structure

```text
RAG-DOCUMENT-LOADER/
├── knowledge-source/
│   ├── apparels.json                  # Sample JSON e-commerce apparel catalog
│   ├── attention_is_all_you_need.pdf  # Benchmark Transformer research paper (NIPS 2017)
│   ├── organizations.csv              # Structured organization dataset
│   └── transformers.txt               # Plain text notes and MCQ Q&A on Transformers
├── notebooks/
│   ├── csv_loader.ipynb               # Tabular data ingestion using CSVLoader
│   ├── pdf_loader.ipynb               # Multi-engine PDF parsing (PyPDF, RapidOCR, PDFMiner, PDFPlumber)
│   └── text_loader.ipynb              # Unstructured text loading with metadata
├── requirement.txt                    # Project dependencies
├── requirements.txt                   # Standard dependency specification
└── README.md
```

---

## 🚀 Implemented Loaders & Notebooks

### 1. PDF Document Parsing (`notebooks/pdf_loader.ipynb`)
Handles complex PDF files with mixed text, embedded images, scanned pages, and tables using four complementary engines:

| Parser / Loader | Description & Best Use Case |
| :--- | :--- |
| **`PyPDFLoader`** | Fast and lightweight parser for standard digital text PDFs. Extracts page-level documents and metadata. |
| **`RapidOCRBlobParser`** | OCR-powered parser using RapidOCR (`onnxruntime`) to extract text from embedded figures, diagrams, and scanned pages. |
| **`PDFMinerLoader`** | Deep layout-preserving parser; extracts text and positions with high precision. |
| **`PDFPlumberLoader`** | Specialized for extracting tabular layouts and precise character positions from PDF reports. |

### 2. Structured Tabular Data (`notebooks/csv_loader.ipynb`)
- Demonstrates loading tabular records with `CSVLoader`.
- Generates one LangChain `Document` per row, preserving column headers as structured metadata for targeted semantic search.

### 3. Plain Text Ingestion (`notebooks/text_loader.ipynb`)
- Loads raw text files using `TextLoader`.
- Captures file metadata (`source`, encoding) alongside `page_content`.

---

## 🛠️ Setup & Installation

1. Create and activate a Python virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
