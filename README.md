# 📚 PaperMind AI

### Intelligent PDF-Based Research Question Answering System

PaperMind AI is an AI-powered research assistant that helps users understand lengthy research papers and technical PDFs. Users can upload a PDF, ask questions in natural language, and receive an answer along with the relevant source page.

## 🚀 How It Works


Research PDF
     ↓
Text Extraction — PyMuPDF
     ↓
Text Cleaning & Chunking
     ↓
Embeddings — all-MiniLM-L6-v2
     ↓
FAISS Semantic Search
     ↓
Hybrid + Section-Aware Retrieval
     ↓
RoBERTa Extractive QA
     ↓
Answer + Source Page


## 🧠 Technologies Used

* Python — Core development
* PyMuPDF — PDF text extraction
* Sentence Transformers — Text embeddings
* all-MiniLM-L6-v2 — Semantic representation
* FAISS — Vector similarity search
* RoBERTa-base-SQuAD2— Extractive question answering
* PyTorch — Deep learning framework
* Hugging Face Transformers — Model and tokenizer handling
* NumPy — Numerical processing
* Google Colab — Development environment

## 🔍 Key Features

* 📄 Upload and process research PDFs
* 🧹 Clean and preprocess extracted text
* ✂️ Split documents into contextual chunks
* 🧠 Generate semantic embeddings
* 🔎 Retrieve relevant information using FAISS
* 🎯 Use hybrid and section-aware retrieval
* 🤖 Extract answers using RoBERTa
* 📌 Identify the source page of the answer

## 💡 Why Hybrid Retrieval?

During development, pure semantic search sometimes retrieved related but incorrect sections. To improve this, the system combines:

Semantic Similarity + Keyword Matching + Section Information

A lightweight rule-based intent detector also identifies questions such as:

* Objective
* Methodology
* Results
* Conclusion
* Technology
* Limitations

This makes the retrieval process more document-aware.

## 🐛 Major Challenges

Some important issues encountered during development included:

* Incorrect sections being retrieved through pure semantic search
* Empty answers with high QA confidence
* Transformers pipeline compatibility issues
* PyTorch/CUDA dependency conflicts
* Deprecated `fitz` API
* `ModuleNotFoundError` for the `src` package
* Notebook function execution-order errors

These challenges helped improve both the retrieval pipeline and the overall understanding of AI system development.

## 🔮 Future Improvements

* Automatic section detection
* Smarter paragraph/sentence-based chunking
* Reranking retrieved passages
* Generative LLM integration
* Multi-document research
* Conversation memory
* OCR for scanned PDFs
* Table and figure understanding
* Persistent vector storage
* Gradio-based web interface
* Evaluation metrics for retrieval and answer accuracy

## 📌 Project Status

Current: Core PDF → Retrieval → QA pipeline implemented.

Next: Transforming the prototype into a more robust, user-friendly research assistant.

## 🎯 Key Learning

The biggest lesson from this project was:

A reliable AI assistant depends on the entire pipeline—not just the model.

Good PDF extraction, chunking, embeddings, retrieval, question answering, and source attribution must work together to produce reliable results. 

 PaperMind AI

Upload. Ask. Retrieve. Understand.

