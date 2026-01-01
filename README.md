# PDF RAG Chatbot

## Overview
This project is an AI-powered **PDF Question Answering system** built using **Retrieval-Augmented Generation (RAG)**.

It answers user questions **strictly based on the content of uploaded PDFs**.  
The system is designed to **avoid hallucinations** and provide **source-backed answers**.

The goal is **document-grounded accuracy**, not conversational creativity.

---

## Problem Statement
Students and researchers often struggle to:
- Extract precise answers from large PDFs
- Search across multiple academic documents
- Verify where an answer actually comes from

Traditional chatbots:
- Hallucinate answers
- Use external knowledge
- Do not provide citations

This project solves the problem by **retrieving exact PDF content first, then generating answers only from it**.

---

## Solution Approach
The chatbot follows a **Retrieval-Augmented Generation (RAG)** pipeline:
1. Retrieve the most relevant PDF chunks
2. Generate answers only from retrieved content
3. Attach clear citations (PDF name + page number)

---

## Input Data (PDF Documents)
- User-uploaded PDF files
- Supported use cases:
  - Lecture notes
  - Research papers
  - Academic textbooks
  - Reports

PDFs are processed dynamically — **no fixed dataset is required**.

---

## How It Works

### 1. PDF Processing
- PDFs are split into smaller text chunks
- Each chunk is tagged with:
  - PDF name
  - Page number
  - Optional subject metadata

---

### 2. Embedding Generation
- Text chunks are converted into vector embeddings
- Semantic meaning is preserved (not keyword-based search)

---

### 3. Vector Storage
- Embeddings are stored using **FAISS**
- Enables fast and scalable similarity search

---

### 4. Query Handling
- User submits a question
- The question is converted into an embedding

---

### 5. Retrieval
- FAISS retrieves the most semantically relevant chunks
- Optional metadata-based filtering is applied

---

### 6. Answer Generation
- Retrieved chunks are passed to the LLM
- Answers are generated **strictly from retrieved content**
- Citations are attached to every response

---

## Why This Is Not a Normal Chatbot
- ❌ No internet access
- ❌ No external knowledge
- ❌ No hallucinated answers

- ✅ PDF-grounded responses only
- ✅ Page-level citations
- ✅ Suitable for academic and exam use

---

## Key Features
- Upload multiple PDFs
- Semantic search using FAISS
- Metadata-based filtering
- Page-wise citations
- Simple gradio interface

---

## Tech Stack
- Python
- gradio
- FAISS
- Sentence Transformers
- groq Model 

---

## Evaluation Philosophy
This system is **not evaluated using accuracy metrics**.

Correctness is determined by:
- Whether the answer exists in the PDFs
- Whether the citation is correct
- Whether hallucination is avoided

If the information is not present, the system responds accordingly.

---

## Cloning the Repository

```bash
git clone https://github.com/yourusername/pdf-rag-chatbot.git
cd pdf-rag-chatbot


