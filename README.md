<div align="center">

# 📚 Multi-PDF RAG Chatbot

<strong>Chat with multiple PDFs at once, in natural language, powered by Retrieval-Augmented Generation (RAG).</strong>

<br>

<img src="https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Streamlit-App-FF4B4B?logo=streamlit&logoColor=white" alt="Streamlit">
<img src="https://img.shields.io/badge/LangChain-RAG-1C3C3C?logo=chainlink&logoColor=white" alt="LangChain">
<img src="https://img.shields.io/badge/FAISS-VectorDB-005571" alt="FAISS">
<img src="https://img.shields.io/badge/Groq-LLM-F55036" alt="Groq">
<img src="https://img.shields.io/badge/License-MIT-green" alt="License">

<br><br>

<img src="https://via.placeholder.com/800x400.png?text=Add+your+demo+screenshot+or+GIF+here" alt="Demo screenshot" width="800">

</div>

<br>

## 📝 About the Project

**Multi-PDF RAG Chatbot** lets you upload one or more PDF documents and ask questions about their content in a real conversation — with follow-up questions and memory, not just single-shot search. Instead of manually scrolling through pages, you get direct answers pulled straight from your documents.

Under the hood, it uses a **Retrieval-Augmented Generation (RAG)** pipeline: your PDFs are broken into chunks, converted into vector embeddings, stored in a local vector database, and retrieved on demand to ground the LLM's answers in your actual documents — instead of relying on the model's own memory (which can hallucinate).

<br>

## ✨ Features

<table>
<tr><td>📂</td><td>Upload <strong>multiple PDFs</strong> at once</td></tr>
<tr><td>💬</td><td>Chat interface with <strong>conversation memory</strong> (handles follow-up questions)</td></tr>
<tr><td>🔍</td><td><strong>Semantic search</strong> over document content using vector embeddings</td></tr>
<tr><td>⚡</td><td>Fast, free inference via <strong>Groq's Llama 3.1</strong></td></tr>
<tr><td>🧠</td><td>Local, free embeddings — no API cost for the retrieval step</td></tr>
<tr><td>🚀</td><td>Deployed live on <strong>Streamlit Community Cloud</strong></td></tr>
</table>

<br>

## 🛠️ Tech Stack

| Layer | Tool |
|---|---|
| UI / App framework | [Streamlit](https://streamlit.io) |
| PDF text extraction | [PyPDF2](https://pypi.org/project/PyPDF2/) |
| Text chunking | LangChain `RecursiveCharacterTextSplitter` |
| Embeddings | HuggingFace `sentence-transformers/all-MiniLM-L6-v2` |
| Vector store | [FAISS](https://github.com/facebookresearch/faiss) |
| LLM | [Groq](https://groq.com) — Llama 3.1 8B Instant |
| Orchestration | [LangChain](https://www.langchain.com) |

<br>

## ⚙️ How It Works

\```
 PDF Upload
     │
     ▼
 Extract raw text (PyPDF2)
     │
     ▼
 Split into overlapping chunks (LangChain)
     │
     ▼
 Convert chunks to embeddings (HuggingFace)
     │
     ▼
 Store in a vector database (FAISS)
     │
     ▼
 User asks a question
     │
     ▼
 Retrieve the most relevant chunks
     │
     ▼
 LLM (Groq / Llama 3.1) generates a grounded answer
     │
     ▼
 Answer + chat history shown in the UI
\```

<br>

## 🚀 Getting Started

### 1. Clone the repo
\```bash
git clone https://github.com/YOUR_USERNAME/multi-pdf-rag-chatbot.git
cd multi-pdf-rag-chatbot
\```

### 2. Install dependencies
\```bash
pip install -r requirements.txt
\```

### 3. Add your API key
Get a free key at [console.groq.com](https://console.groq.com), then create a `.env` file:
\```
GROQ_API_KEY=your_key_here
\```

### 4. Run the app
\```bash
streamlit run app.py
\```

<br>

## 🌐 Live Demo

<div align="center">

**[👉 Try it live here](https://your-app-name.streamlit.app)**

</div>

<br>

## 📌 Future Improvements

- [ ] Hybrid search (keyword + semantic) for better retrieval accuracy
- [ ] Support for scanned/image-based PDFs via OCR
- [ ] Answer evaluation pipeline (RAGAS) to measure hallucination
- [ ] Source citations shown alongside each answer
- [ ] Support for additional file types (docx, txt)

<br>

## 🤝 Connect

<div align="center">

Built by **[Your Name]** — feel free to connect or reach out!

<a href="https://www.linkedin.com/in/your-linkedin/">LinkedIn</a> •
<a href="https://github.com/YOUR_USERNAME">GitHub</a>

</div>
