# Awesome Retrieval-Augmented Generation (RAG)

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/thiernodaoudaly/awesome-rag?style=social)](https://github.com/thiernodaoudaly/awesome-rag/stargazers)
[![License](https://img.shields.io/github/license/thiernodaoudaly/awesome-rag)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Last Commit](https://img.shields.io/github/last-commit/thiernodaoudaly/awesome-rag)](https://github.com/thiernodaoudaly/awesome-rag/commits)

## Table of Contents

* [Introduction](#introduction)
* [Latest Papers](#latest-papers)
* [Foundations](#foundations)
* [Advanced RAG Techniques](#advanced-rag-techniques)
* [RAG Architectures & Pipelines](#-rag-architectures--pipelines)
* [RAG Design Patterns](#-rag-design-patterns)
* [End-to-End RAG Stack](#-end-to-end-rag-stack)
* [RAG Evaluation Pipeline](#-rag-evaluation-pipeline)
* [Advanced Topics](#-advanced-topics)
* [Evaluation & Benchmarks](#evaluation--benchmarks)
* [Tools & Frameworks](#tools--frameworks)
* [Vector Databases](#vector-databases)
* [Applications](#applications)
* [Trends](#trends)
* [Resources](#resources)
* [Contributing](#contributing)
* [License](#license)

## Introduction

**[Retrieval-Augmented Generation (RAG)](https://arxiv.org/abs/2005.11401)** combines **retrieval** and **generation** to build reliable, factual, and scalable AI systems.

## Latest Papers

* **[Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401)**

  > Introduces the RAG framework combining retrieval and generation.

* **[Self-RAG: Learning to Retrieve, Generate, and Critique](https://arxiv.org/abs/2310.11511)**

  > Enables LLMs to retrieve, generate, and self-evaluate outputs.

* **[Corrective RAG (CRAG)](https://arxiv.org/abs/2401.15884)**

  > Improves factual accuracy by correcting retrieved information.

* **[RAG-Fusion](https://arxiv.org/abs/2402.03367)**

  > Combines multiple retrieval strategies for better performance.

## Foundations

* **[Dense Passage Retrieval (DPR)](https://arxiv.org/abs/2004.04906)**

  > Introduces dense vector-based retrieval for open-domain QA.

* **[REALM](https://arxiv.org/abs/2002.08909)**

  > Pre-trains language models with retrieval augmentation.

## Advanced RAG Techniques

* **[Multi-hop RAG](https://arxiv.org/search/?query=multi-hop+rag&searchtype=all)**

  > Enables reasoning across multiple retrieved documents.

* **[Hybrid Search (BM25 + Embeddings)](https://arxiv.org/search/?query=hybrid+search+bm25+embedding&searchtype=all)**

  > Combines sparse and dense retrieval methods.

* **[Query Rewriting](https://arxiv.org/search/?query=query+rewriting+retrieval&searchtype=all)**

  > Improves retrieval by reformulating queries.

* **[Reranking Models](https://arxiv.org/search/?query=reranking+retrieval+models&searchtype=all)**

  > Reorders retrieved results using more precise models.

* **[Context Compression](https://arxiv.org/search/?query=context+compression+llm&searchtype=all)**

  > Reduces context size while preserving key information.

## RAG Architectures & Pipelines

### 🔹 Basic RAG Pipeline

```
User Query
    ↓
Query Encoder
    ↓
Vector Database (Retrieval)
    ↓
Top-K Documents
    ↓
LLM (Generator)
    ↓
Final Answer
```

Reference:

* **[RAG Paper](https://arxiv.org/abs/2005.11401)**
* **[Dense Passage Retrieval](https://arxiv.org/abs/2004.04906)**

### 🔹 Advanced RAG Pipeline (Production-Ready)

```
User Query
    ↓
Query Rewriting
    ↓
Hybrid Retrieval (BM25 + Embeddings)
    ↓
Reranker (Cross-Encoder)
    ↓
Context Compression
    ↓
LLM (Generation)
    ↓
Post-processing (Citations, Formatting)
```

Related:

* **[RAG-Fusion](https://arxiv.org/abs/2402.03367)**
* **[Self-RAG](https://arxiv.org/abs/2310.11511)**

### Agentic RAG (Next-Gen)

```
User Query
    ↓
LLM Agent
    ↓
Tool Selection
    ↓
Retriever / APIs / DB
    ↓
Multi-step Reasoning
    ↓
Final Answer
```

Related:

* **[Toolformer](https://arxiv.org/abs/2302.04761)**
* **[ReAct](https://arxiv.org/abs/2210.03629)**

### Multi-Hop RAG

```
Query → Retrieve → Reason → Retrieve → Answer
```

Explore:

* https://arxiv.org/search/?query=multi-hop+rag&searchtype=all

## RAG Design Patterns

### 🔸 Chunking Strategies

* Fixed-size chunking
* Semantic chunking
* Sliding window

🔗 https://arxiv.org/search/?query=text+chunking+nlp

### 🔸 Retrieval Strategies

* Dense retrieval
* Sparse retrieval (BM25)
* Hybrid retrieval

🔗 https://arxiv.org/search/?query=hybrid+retrieval+bm25

### 🔸 Reranking

* Cross-encoders
* LLM-based reranking

🔗 https://arxiv.org/search/?query=reranking+retrieval

### 🔸 Context Optimization

* Context compression
* Top-K filtering
* Token budgeting

🔗 https://arxiv.org/search/?query=context+compression+llm

## End-to-End RAG Stack

### 🔹 Minimal Stack

* Embeddings → [OpenAI](https://platform.openai.com/) / [SentenceTransformers](https://www.sbert.net/)
* Vector DB → [FAISS](https://github.com/facebookresearch/faiss)
* LLM → [OpenAI](https://platform.openai.com/) / [Hugging Face](https://huggingface.co/)

### 🔹 Production Stack

* Orchestration → [LangChain](https://github.com/langchain-ai/langchain) / [LlamaIndex](https://github.com/jerryjliu/llama_index)
* Vector DB → [Pinecone](https://www.pinecone.io/) / [Weaviate](https://weaviate.io/)
* Monitoring → [LangSmith](https://smith.langchain.com/)
* Evaluation → https://arxiv.org/abs/2309.15217

## RAG Evaluation Pipeline

```
Dataset → Retrieval Evaluation → Generation Evaluation → Human Evaluation
```

* **[BEIR Benchmark](https://arxiv.org/abs/2104.08663)**
* **[RAG Evaluation](https://arxiv.org/abs/2309.15217)**

## Advanced Topics

* [RAG + Agents](https://arxiv.org/search/?query=rag+agents)
* [Self-RAG](https://arxiv.org/abs/2310.11511)
* [Real-time RAG](https://arxiv.org/search/?query=real+time+rag)
* [Enterprise RAG](https://arxiv.org/search/?query=enterprise+rag)

## Visual Resources

* [LangChain](https://github.com/langchain-ai/langchain)
* [LlamaIndex](https://github.com/jerryjliu/llama_index)
* [Weaviate Blog](https://weaviate.io/blog)

## Featured Implementations

* [LangChain](https://github.com/langchain-ai/langchain)
* [LlamaIndex](https://github.com/jerryjliu/llama_index)
* [Haystack](https://github.com/deepset-ai/haystack)

## Evaluation & Benchmarks

* **[BEIR Benchmark](https://arxiv.org/abs/2104.08663)**

  > Benchmark for retrieval evaluation.

* **[RAG Evaluation Techniques](https://arxiv.org/abs/2309.15217)**

  > Methods to evaluate RAG systems.

## Tools & Frameworks

* [LangChain](https://github.com/langchain-ai/langchain)
* [LlamaIndex](https://github.com/jerryjliu/llama_index)
* [Haystack](https://github.com/deepset-ai/haystack)
* [Semantic Kernel](https://github.com/microsoft/semantic-kernel)

## Vector Databases

* [FAISS](https://github.com/facebookresearch/faiss)
* [Pinecone](https://www.pinecone.io/)
* [Weaviate](https://weaviate.io/)
* [Chroma](https://github.com/chroma-core/chroma)

## Applications

* [Document QA](https://arxiv.org/search/?query=document+qa+rag&searchtype=all)
* [Chatbots with Memory](https://arxiv.org/search/?query=rag+chatbot+memory&searchtype=all)
* [Enterprise Search](https://arxiv.org/search/?query=enterprise+search+rag&searchtype=all)
* [Code Assistants](https://arxiv.org/search/?query=code+assistant+rag&searchtype=all)

## Trends

* [RAG + Agents](https://arxiv.org/search/?query=rag+agents)
* [Self-RAG Systems](https://arxiv.org/search/?query=self+rag)
* [Real-Time Retrieval](https://arxiv.org/search/?query=real+time+retrieval+llm)
* [Enterprise RAG](https://arxiv.org/search/?query=enterprise+rag)

## Resources

* [Papers with Code – RAG](https://paperswithcode.com/search?q=rag)
* [GitHub RAG Search](https://github.com/search?q=rag&type=repositories)
* [ArXiv RAG Papers](https://arxiv.org/search/?query=retrieval+augmented+generation&searchtype=all)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md)

## License

This project is licensed under the MIT License.
See [LICENSE](LICENSE) for details.
