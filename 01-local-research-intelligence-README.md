# Local Research Intelligence & Agentic RAG

A local research assistant for analyzing technical documents and research papers using semantic retrieval, source-grounded generation, and lightweight agentic workflows.

> **Status:** Planned / Under Development  
> The repository currently defines the project architecture and development plan. Features will be updated as they are implemented and evaluated.

## Overview

The goal of this project is to build a research assistant that can work with technical PDFs without depending on paid proprietary APIs.

The system will:

- ingest technical PDF documents
- extract and clean text
- split documents into meaningful chunks
- generate semantic embeddings
- retrieve relevant passages using vector search
- generate answers using a local/open-source language model
- provide citations to retrieved source passages
- support lightweight tool-based research workflows
- evaluate retrieval and answer quality

## Problem

Technical papers can be long and difficult to search using traditional keyword-based methods. A research assistant should understand semantic similarity and retrieve the parts of a document that are relevant to a user's question.

The project therefore focuses on **Retrieval-Augmented Generation (RAG)** rather than relying only on an LLM's pretrained knowledge.

## Architecture

```text
PDF / Research Papers
        |
        v
Document Extraction
        |
        v
Text Cleaning
        |
        v
Chunking
        |
        v
Embedding Generation
        |
        v
Vector Search
        |
        v
Relevant Context
        |
        v
Local LLM
        |
        v
Source-Cited Answer
        |
        v
Evaluation / Logging
```

## Agentic Layer

A lightweight agentic layer will be introduced only where it provides a clear benefit.

Potential tools include:

- document search
- semantic retrieval
- source inspection
- document summarization
- document comparison
- structured research workflows

The project intentionally avoids unnecessary multi-agent complexity.

## Planned Features

### Document Processing
- PDF ingestion
- text extraction
- chunking
- metadata preservation

### Retrieval
- local embedding generation
- vector indexing
- top-k semantic retrieval
- similarity scoring

### Generation
- local/open-source LLM inference
- context-aware prompting
- source-grounded responses

### Citations
Responses should identify the document and relevant source passage used to generate the answer.

### Evaluation
The project will evaluate:

- retrieval relevance
- top-k retrieval quality
- citation correctness
- answer grounding
- missing-evidence behaviour
- conflicting-source behaviour
- latency

## Technology Stack

- Python
- PyMuPDF
- Sentence Transformers
- FAISS or Qdrant
- Ollama
- Open-source LLM
- FastAPI
- SQLite where useful
- Docker where useful

## Planned Repository Structure

```text
local-research-intelligence/
├── app/
│   ├── ingestion/
│   ├── retrieval/
│   ├── generation/
│   ├── agents/
│   └── api/
├── evaluation/
├── data/
├── tests/
├── notebooks/
├── requirements.txt
├── README.md
└── .gitignore
```

## Development Plan

1. Build PDF ingestion.
2. Implement text chunking.
3. Generate local embeddings.
4. Build vector search.
5. Add local LLM generation.
6. Add source citations.
7. Expose the pipeline through a simple API.
8. Add lightweight agentic tools.
9. Build an evaluation set.
10. Measure retrieval and answer quality.
11. Document failure cases and limitations.

## Expected Learning Outcomes

- Embeddings
- Vector databases/search
- Retrieval-Augmented Generation
- Local LLM inference
- Prompt/context construction
- Agentic workflows
- API development
- Evaluation of LLM systems
- Software engineering

## Design Principles

- Local/open-source first
- No unnecessary paid API dependency
- Simple architecture before advanced frameworks
- Reproducible experiments
- Explicit evaluation
- Transparent citations
- Documented limitations
