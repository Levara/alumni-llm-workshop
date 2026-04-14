# Alumni LLM Workshop

Hands-on workshop building LLM applications from first API calls to production RAG systems. Five sessions, each with a lecture and a Google Colab notebook.

**Lectures:** [preze.levara.xyz/preze/llm-rag-workshop/popis.html](https://preze.levara.xyz/preze/llm-rag-workshop/popis.html)

## Sessions

### 01 — LLM API Fundamentals

Build an AI quiz game. Covers chat completions, statelessness, system prompts, structured XML output, reasoning models, and prompt engineering.

**Notebook:** `01_llm_api_fundamentals.ipynb`

### 02 — Embeddings & Semantic Search

Turn text into vectors and build a semantic search engine from scratch. Covers embeddings, cosine similarity, batch embedding, and the limits of similarity (similar ≠ correct).

**Notebook:** `02_embeddings_intro.ipynb`

### 03 — ChromaDB Vector Database

Replace the in-memory search engine with a real vector database. Covers ChromaDB collections, auto-embedding, metadata filtering, and CRUD operations.

**Notebook:** `03_chromadb_basics.ipynb`

### 04 — RAG Pipeline

Build a complete Retrieval-Augmented Generation system over ~4,100 Croatian Wikipedia articles. Covers chunking strategies (fixed vs. section-based), embedding a real corpus, retrieval + generation, and grounded answers.

**Notebook:** `04_rag_pipeline.ipynb`

### 05 — Advanced RAG & Evaluation

Enhance the RAG pipeline with hybrid search (BM25 + semantic + RRF fusion), cross-encoder reranking, query rewriting, confidence thresholds, citation-aware generation, and rigorous evaluation (P@K, R@K, MRR, LLM-as-Judge).

**Notebook:** `05_advanced_rag.ipynb`

## Corpus

Sessions 1–3 use `usa-iran-corpus.txt` (23 English articles about the 2026 Iran War). Sessions 4–5 use Croatian Wikipedia articles extracted from the hrwiki dump. See [WIKI-HR.md](WIKI-HR.md) for details on the extraction pipeline.

## Infrastructure

Sessions 1–3 use [OpenRouter](https://openrouter.ai) (cloud API). Sessions 4–5 use self-hosted models via [vLLM](https://github.com/vllm-project/vllm) behind a reverse proxy at `llmapi.levara.xyz`.
