# HyperGraphCAG

HyperGraphCAG (Hypergraph-based Retrieval Augmented Generation with Semantic Cache) is an advanced RAG framework that combines **structured knowledge representation using hypergraphs** with **efficient response generation via semantic caching**.

<img width="700" alt="Image" src="https://github.com/user-attachments/assets/8282b215-f3cd-4bac-86e2-0fcb21e43b66" />

## ⚙️ System Architecture

### 1. Knowledge Construction  
Domain-specific documents are segmented into text chunks. A language model extracts entities and relations to build a **knowledge hypergraph**, where each hyperedge connects two or more entities through a descriptive relation.

### 2. Hypergraph-Guided Retrieval  
At query time, a semantic search retrieves the most relevant entities and hyperedges from the hypergraph based on cosine similarity. These are expanded into a **subgraph** that captures the relevant context for the query.

### 3. Cache-Based Generation  
The selected subgraph and its associated textual chunks are preprocessed and stored in a **semantic cache**. During inference, this cache is directly loaded into the model’s memory, enabling **low-latency and cost-free** response generation without external API calls.

## 🚀 Key Features

- Hypergraph-based structured knowledge representation  
- Semantic search with graph-guided retrieval  
- Efficient, cache-based generation with minimal latency  
- Fully open-source and offline-compatible setup  

## 📌 Future Work

Planned improvements include:

- Extending cache memory capacity to overcome LLM context limitations  
- Enhancing entity and relation extraction accuracy  
- Optimizing the cost and scalability of the cache construction phase

## 🧑‍💻 Author

**Francesco Della Valle**  
Master's Thesis in Big Data Engineering  
University of Naples "Federico II"  
Academic Year 2024/2025
