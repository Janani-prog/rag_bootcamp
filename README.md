# RAG_Basics
This repository is a hands-on introduction to Retrieval-Augmented Generation (RAG) using Python, LangChain, OpenAI, and local vector stores. It is designed for those who want to learn how to combine Large Language Models (LLMs) with custom knowledge sources (like PDFs) to build question-answering systems.

## What is RAG?
Retrieval-Augmented Generation (RAG) is a technique that enhances LLMs by allowing them to retrieve relevant information from external data sources (such as documents or databases) before generating a response. This approach enables more accurate and context-aware answers, especially when the required knowledge is not part of the model’s training data.

## What does this repo do?

- Shows how to generate embeddings** for text using both local models (e.g., SentenceTransformers) and cloud APIs (OpenAI).
- Demonstrates how to extract and chunk text** from PDFs for use as a knowledge base.
- Builds a vector store** (using FAISS) to enable efficient similarity search over your document chunks.
- Connects a vector store to an LLM** (OpenAI’s GPT models) using LangChain, so you can ask questions and get answers grounded in your own documents.
- Includes Jupyter notebooks** that walk through each step, from data preparation to running a full RAG pipeline.

## Example Workflow

1. Extract text from PDF:  
   Use PyPDF2 to read a PDF and split it into manageable text chunks.

2. Generate embeddings:  
   Use OpenAI or SentenceTransformers to convert text chunks into vector representations.

3. Build a vector store:
   Store the embeddings in a FAISS index for fast retrieval.

4. Ask questions:
   When you ask a question, the system retrieves the most relevant chunks from your documents and feeds them to the LLM to generate an answer.

## Main Files

- `RAG_withOpenai.ipynb` — End-to-end example using OpenAI for embeddings and LLM.
- `Embeddings_generation_withOllama.ipynb` — Example using Ollama for local embeddings.
- `01-langchain_Basics.ipynb`, `02-langchain_Prompts.ipynb`, `03-langchain_chains.ipynb` — Step-by-step LangChain tutorials.
- `1. dietary supplements - for whom.pdf` — Sample PDF used as a knowledge source.
- `myVectorStore/`, `health_supplements/` — Example FAISS vector store directories.

## Getting Started

1. install dependencies
   ```sh
   pip install -r requirements.txt
   ```

2. **Set your OpenAI API key**  
   Create a `.env` file in the root directory:
   ```
   OPENAI_KEY=your_openai_api_key
   ```

3. Run the notebooks
   Open any notebook in Jupyter or VS Code and follow the instructions.

## Who is this for?

- Developers interested in LLMs, RAG, and document-based QA.
- Anyone wanting to build chatbots or assistants that can answer questions using their own documents.
