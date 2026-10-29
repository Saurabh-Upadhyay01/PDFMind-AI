📚 RAG-Based Document Chatbot

A local Retrieval-Augmented Generation (RAG) chatbot that allows users to upload PDF documents and ask natural-language questions about their content.

The chatbot processes the uploaded document, converts the content into vector embeddings, retrieves the most relevant information, and generates answers using a locally running LLM.

📌 Project Overview

This project implements a Retrieval-Augmented Generation (RAG) pipeline for document-based question answering.

Users can upload a PDF through a Streamlit interface and ask questions related to the uploaded document.

The system:

Extracts text from the PDF
Splits the document into smaller chunks
Generates vector embeddings
Stores the embeddings in ChromaDB
Performs semantic similarity search
Retrieves the most relevant document chunks
Sends the retrieved context to Gemma 2B
Generates an answer based only on the uploaded document

The project runs locally using Ollama and does not require a paid API.

✨ Features
📄 Upload PDF documents
🔍 Extract text from PDFs
✂️ Split documents into smaller chunks
🧠 Generate embeddings using Nomic Embed Text
🗄️ Store embeddings using ChromaDB
🔎 Perform semantic similarity search
🤖 Generate answers using Gemma 2B
💬 Interactive Streamlit chatbot interface
🔒 Local processing using Ollama
💰 No paid API required this is not there

## 🏗️ Architecture

```text
PDF Upload
     ↓
PDF Text Extraction
     ↓
Text Chunking
     ↓
Nomic Embed Text
     ↓
Vector Embeddings
     ↓
ChromaDB
     ↓
Similarity Search
     ↓
Relevant Document Chunks
     ↓
Gemma 2B
     ↓
Generated Answer
```

---

## 🛠️ Technologies Used
| Technology | Purpose |
|-----------|---------|
| Python | Core programming language |
| LangChain | RAG pipeline and document processing |
| PyPDF | PDF text extraction |
| Nomic Embed Text | Document embeddings |
| ChromaDB | Vector database |
| Ollama | Local model execution |
| Gemma 2B | Local language model |
| Streamlit | Web-based chatbot interface |
---

## 📁 Project Structure

```text
RAG-Document-Chatbot/
│
├── app.py
├── rag.py
├── test_rag.py
├── requirements.txt
├── README.md
├── .gitignore
└── venv/
```

---


### 2. Create a Virtual Environment

On Windows:

```bash
python -m venv venv
```

Activate the environment:

```powershell
.\venv\Scripts\Activate.ps1
```

If PowerShell gives an execution-policy error, run:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
```

Then activate again:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🦙 Ollama Setup

This project uses Ollama to run the models locally.

Download the embedding model:

```bash
ollama pull nomic-embed-text
```

Download the language model:

```bash
ollama pull gemma2:2b
```

Check the installed models:

```bash
ollama list
```

You should see:

```text
nomic-embed-text
gemma2:2b
```

---

## ▶️ How to Run

Make sure the virtual environment is activated.

Run:

```bash
streamlit run app.py
```

Streamlit will start the chatbot application in your browser.

---

## 💬 How to Use

### Step 1 — Upload a PDF

Open the Streamlit application and upload a PDF document.

### Step 2 — Document Processing

The application processes the document through the following pipeline:

```text
PDF
 ↓
Text Extraction
 ↓
Chunking
 ↓
Embeddings
 ↓
ChromaDB
```

### Step 3 — Ask a Question

Enter a question related to the uploaded document.

For example:

```text
What is the main topic of this document?
```

### Step 4 — Generate Answer

The chatbot retrieves the most relevant document chunks and sends them to Gemma 2B.

Gemma generates the final answer using the retrieved document context.

---


## 🚀 Future Improvements

Possible future improvements include:

- Support for multiple PDF uploads
- Support for DOCX and TXT files
- Conversation memory
- Source and page citations
- Improved document retrieval
- Hybrid search
- Reranking retrieved documents
- Streaming responses
- Chat history
- Docker deployment
- Cloud deployment
- Authentication and user management

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience with:

- Retrieval-Augmented Generation
- Large Language Models
- Vector databases
- Semantic search
- Document embeddings
- LangChain
- Ollama
- ChromaDB
- Streamlit
- PDF document processing
- End-to-end AI application development

---
