# 📘 PDF Question Answering (QA) System 

This repository contains the implementation of a **PDF-based Question Answering system**. The project leverages **LangChain, Amazon Bedrock, and FAISS** to enable accurate retrieval and response from technical documents, supported with both **text and images**.  

---

## 🔹 Purpose of Included Files

- **`PDF_QnA.ipynb`** → A Python notebook demonstrating the **end-to-end Q&A pipeline** with text + image support.  
- **`HP_printer_manual.pdf`** → A sample **technical manual** (HP printer) serving as test data for the pipeline.  

---
## 🔹 Key Features

- **PDF Content Extraction**
  - Uses **PyMuPDF** to parse PDF files and extract both **text and images**.  
  - Images are encoded into **base64 format** for seamless integration with prompts.  

- **Embeddings & Vector Store**
  - Extracted text is chunked and embedded using **Amazon Titan (`amazon.titan-embed-text-v2`)**.  
  - Embedded vectors are stored in a **FAISS vector store** for efficient semantic similarity search.  

- **Retrieval-Augmented Generation (RAG)**
  - User queries trigger semantic search in FAISS to retrieve the most **relevant text chunks**.  
  - The retrieved text, along with related **base64-encoded images**, is used to **construct a context-rich prompt**.  

- **Answer Generation with Claude**
  - Prompts are sent to **Claude (`anthropic.claude-3-sonnet-v1`)** via **Amazon Bedrock**.  
  - Claude generates **context-aware answers** that may include references to corresponding images.  

- **Notebook Visualization**
  - In **Jupyter Notebook**, images are automatically **decoded and rendered inline** along with the answers.  
  - This provides a complete, interactive experience for exploring technical documents.  

---

## 🔹 Setup Instructions

- Clone the repository and install dependencies.  
- Replace the placeholders in your environment with actual AWS credentials
- Open **`PDF_QnA.ipynb`** and follow the step-by-step process to test the pipeline on the sample PDF.  

---

## ✅ Project Status

This is an **ongoing project (POC)** for building a robust, visually-supported **RAG-based Question Answering system** for technical documents.   


