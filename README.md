# HyperGraphCAG

**HyperGraphCAG** (Hypergraph-based Retrieval Augmented Generation with Semantic Cache) is an advanced RAG framework that combines **structured knowledge representation using hypergraphs** with **efficient response generation via semantic caching**.

## 🧠 Project Description

- Modeling knowledge through **hypergraphs** to capture **n-ary relations** between entities
- Leveraging a **hypergraph-guided retrieval** mechanism for more accurate context selection
- Employing **Cache-Augmented Generation (CAG)** to allow fast and **retrieval-free inference**

![System Architecture](HGCag.drawio.png)

## ⚙️ System Architecture

The system is composed of three main phases:

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
