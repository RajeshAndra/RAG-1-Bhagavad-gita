# RAG-1: Bhagavad-gita Repository

This repository implements a Retrieval-Augmented Generation (RAG) pipeline using embeddings stored in a FAISS database. The project uses a **Bhagavad-gita PDF** to extract textual content and perform similarity search and other operations. The pipeline integrates Gemini API for language model interactions and utilizes various tools like LangChain, SentenceTransformers, and FAISS.

---

## Features

- Extract content from the Bhagavad-gita PDF using PyMuPDF (`fitz`).
- Generate embeddings for the content using `SentenceTransformer`.
- Store and retrieve embeddings in/from a FAISS database.
- Perform similarity search and retrieval-augmented generation (RAG) using embeddings.
- Interact with the Gemini API for advanced language processing and augmentation.

---

## Installation

### Clone the Repository
```bash
git clone https://github.com/RajeshAndra/RAG-1-Bhagavad-gita.git
cd RAG-1-Bhagavad-gita
```

### Configure Environment Variables
Rename the `.env_sample` file to `.env` and add your Gemini API key:
```
GEMINI_API_KEY = A_1hsi***iKs-19w
```

### Install Dependencies
Install the required Python libraries:
```bash
pip install -r requirements.txt
```

---

## Usage

### Load and Store Embeddings into FAISS Database

Below is a high-level overview of the code functionality for handling embeddings with FAISS:

1. **Load PDF and Extract Text**  
   The Bhagavad-gita PDF is loaded using `PyMuPDF`, and its content is extracted for processing.

2. **Generate Embeddings**  
   The extracted text is encoded into vector embeddings using the `SentenceTransformer` library.

3. **Store Embeddings**  
   Store the generated embeddings into a FAISS database for efficient similarity search.

4. **Retrieve Embeddings**  
   Perform similarity search in the FAISS database using input queries.

5. **Interact with Gemini API**  
   Use the embeddings for retrieval-augmented generation with the Gemini language model.

---

## Key Files

- `main.py`: Core script for loading, processing, and interacting with the RAG pipeline.
- `.env_sample`: Template file for environment variables.
- `requirements.txt`: List of dependencies required for the project.
