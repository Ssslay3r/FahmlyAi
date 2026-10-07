# Fahmly AI / RAG

This directory is reserved for AI-specific logic integrated by the shared FastAPI backend. It is part of the modular monolith, not a separate microservice. Flutter and Next.js will access AI capabilities through the backend.

## Directory Purposes

- `rag/ingestion/`: future text extraction and cleaning of uploaded documents.
- `rag/chunking/`: splitting extracted text into useful retrieval units.
- `rag/embeddings/`: document and query embedding generation.
- `rag/retrieval/`: semantic search over chunks stored with pgvector.
- `rag/generation/`: constructing relevant context and generating grounded answers through an LLM.
- `prompts/system/`: shared system instructions.
- `prompts/explanation/`: explanation prompt templates.
- `prompts/summarization/`: summarization prompt templates.
- `prompts/quiz/`: quiz-generation prompt templates.
- `prompts/libyan_dialect/`: prompts supporting natural Libyan dialect.
- `evaluation/`: future evaluation methods, configurations, and reference assets.
- `experiments/`: exploratory AI work; private documents and generated data must remain excluded from Git.

Executable system-level AI checks will live in `tests/ai-evaluation/`; coordinate these with the evaluation assets here.

## Expected RAG Flow

Approximate planned flow:

```text
Uploaded Document
  -> Text Extraction
  -> Cleaning
  -> Chunking
  -> Embedding Generation
  -> pgvector
  -> User Question
  -> Query Embedding
  -> Semantic Retrieval
  -> Relevant Context
  -> LLM
  -> Grounded Answer
```

Document ingestion builds the chunk index in PostgreSQL / pgvector. At question time, the query embedding retrieves relevant chunks from that index before the LLM receives context. Original documents will be stored in Object Storage.

Keep providers replaceable where practical and keep API keys on the backend. Evaluation will cover retrieval quality, answer grounding, Arabic, and Libyan dialect support. No pipeline, prompts, or provider integrations have been implemented yet.
