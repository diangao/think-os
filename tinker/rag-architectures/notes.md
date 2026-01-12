# RAG Architectures

> Exploring different approaches to Retrieval-Augmented Generation

---

## Questions

- How to chunk documents effectively?
- Vector DB vs traditional search: when to use which?
- How to handle citations/sources?

## Resources

- [LangChain RAG docs](https://langchain.com)
- "RAG from Scratch" video series
- Pinecone blog posts on embeddings

## Experiments

### 2026-01-08: Simple RAG prototype

Tried basic RAG with:
- Document chunking (500 tokens, 50 overlap)
- OpenAI embeddings
- FAISS for vector search

**Findings**:
- Works well for factual Q&A
- Struggles with multi-hop reasoning
- Need better chunking strategy for code

**Next**: Try semantic chunking instead of fixed-size

---

## Ideas

- Build a personal knowledge RAG over my notes
- Compare different embedding models (OpenAI vs local)
- Hybrid search: vector + keyword

---
