# 📄 PDF RAG Chatbot

An AI-powered chatbot that answers questions based strictly on the content of uploaded PDFs using **Retrieval-Augmented Generation (RAG)**. Perfect for academic study, research, or knowledge management.

## Features

- Upload multiple PDFs and ask precise questions.
- Semantic search using **FAISS** to find the most relevant chunks.
- Metadata-based filtering to retrieve subject-specific content.
- Clean citations for sources.
- Streamlit web interface for easy interaction.

## Screenshots

*(Add your screenshots here if available)*

## How It Works

1. **Upload PDFs** – PDFs are split into chunks and converted into embeddings.
2. **Metadata Tagging** – Each chunk is tagged with PDF name, page number, and optionally, subject.
3. **Query** – User asks a question.
4. **Retrieval** – FAISS finds semantically similar chunks across all PDFs.
5. **Filtering** – Only relevant chunks (e.g., subject-specific) are selected.
6. **Answer Generation** – Chatbot returns the answer with citations.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/pdf-rag-chatbot.git
cd pdf-rag-chatbot
