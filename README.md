# 🚀 PodRAG AI — Query Any Podcast Using RAG

PodRAG AI is an AI-powered system that allows users to intelligently query long podcast transcripts using **Retrieval-Augmented Generation (RAG)**.

Unlike basic implementations, this project focuses on **retrieval optimization**, improving answer quality by designing an efficient pipeline.

---

## 🧠 Overview

Understanding long podcast content is difficult.

PodRAG AI solves this by:
- Breaking transcripts into meaningful chunks  
- Retrieving the most relevant context  
- Generating accurate, grounded answers  

---

## ⚙️ System Architecture
 Transcript → Chunk → Embed → Store (FAISS)
 Query → Retrieve (MMR) → Context → LLM → Answer

---

## 🔧 Tech Stack

- **LLM**: OpenRouter (Claude / GPT models)  
- **Embeddings**: HuggingFace (Sentence Transformers)  
- **Vector Database**: FAISS  
- **Framework**: LangChain  

---

## 🔍 Key Features

### 🔹 Optimized Chunking
- Recursive chunking strategy  
- `chunk_size = 500`  
- `chunk_overlap = 100`  

→ Preserves conversational flow in transcripts  

---

### 🔹 Advanced Retrieval (MMR)
- `k = 5`, `fetch_k = 10`  
- Reduces redundancy  
- Improves diversity and relevance of results  

---

### 🔹 Context-Grounded Responses
- Retrieved chunks passed to LLM  
- Answers generated strictly from context  
- Reduces hallucination  

---

## 💡 Key Learnings

- Retrieval quality impacts results more than the LLM  
- Chunking strategy significantly affects accuracy  
- MMR improves retrieval diversity  
- RAG is fundamentally a **search + ranking system**  
