# RAG Text Splitter & Chunking Strategies (Upcoming)

This module focuses on document splitting and chunking techniques in Retrieval-Augmented Generation (RAG). Chunking is one of the most critical stages in the RAG pipeline—it determines the granularity, context quality, and retrieval accuracy for downstream embeddings and vector search.

---

## 📌 Planned Topics & Implementations

- [ ] **Character & Recursive Character Text Splitting**:
  - `CharacterTextSplitter`: Simple character-based window splitting.
  - `RecursiveCharacterTextSplitter`: Recursively splitting by paragraphs, sentences, and words to preserve semantic structure.
- [ ] **Token-Based Splitting**:
  - `TokenTextSplitter` and `tiktoken`: Ensuring chunks fit model token context windows without abrupt truncations.
- [ ] **Code & Markdown Structure Splitting**:
  - `MarkdownHeaderTextSplitter`: Preserving header hierarchy and contextual metadata.
  - `PythonCodeTextSplitter` / `Language`-based splitters: Syntax-aware chunking for programming languages.
- [ ] **Semantic Chunking**:
  - Embedding distance and cosine similarity breakpoint detection to split text based on shifts in topic/meaning.
- [ ] **Context-Aware / Agentic Chunking**:
  - Small-to-big retrieval (parent-child chunking) and summary-based metadata enrichment.

---

## 📂 Expected Structure

```text
RAG-TEXT-SPLITTER/
├── notebooks/
│   ├── recursive_character_splitter.ipynb
│   ├── token_splitter.ipynb
│   ├── markdown_splitter.ipynb
│   └── semantic_chunking.ipynb
├── requirements.txt
└── README.md
```

*Stay tuned as notebooks and exercises are added to this module!*
