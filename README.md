# RAG-based Question-Answering System for LaTeX Documentation

This repository contains our final project for the *Introduction to Text Analytics* course, where we developed a **Retrieval-Augmented Generation (RAG)** pipeline to answer questions about LaTeX using Overleaf's official documentation as the source.

## 🚀 Project Overview

We implemented a RAG-based Q&A system using various retrieval techniques and large language models (LLMs). The system takes a user's question about LaTeX, retrieves relevant documentation chunks, and then generates a detailed and contextual answer using a pre-trained LLM.

## 📊 Key Features

- 🧠 Semantic Search (FAISS, BM25, TF-IDF)
- 🤖 LLMs for answer generation: Zephyr-7B, Mistral-7B, Qwen-3B, Gemma-3B
- 📚 Custom-scraped dataset from Overleaf’s Learn portal (151+ LaTeX guides)
- 🧩 Chunking with overlap for better contextual retrieval
- ✅ Custom evaluation metric for **relevance score** based on semantic similarity
- ⚠️ Discussion on faithfulness metrics and limitations

## 📁 Dataset

We scraped and structured the Overleaf LaTeX Learn documentation using BeautifulSoup. Each guide was parsed for headings, paragraphs, lists, and code blocks and saved in a JSON format.

```json
{
  "title": "Inserting Images",
  "url": "https://www.overleaf.com/learn/latex/Inserting_Images",
  "content": [
    {"type": "heading", "data": "Captioning"},
    {"type": "text", "data": "Captions help..."},
    {"type": "code", "data": "\\includegraphics[..."}
  ]
}
