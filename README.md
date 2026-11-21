AI Research Article Assistant using RAG

Project Overview

AI Research Article Assistant is a Generative AI-based application built using Retrieval-Augmented Generation (RAG). It allows users to upload PDF research articles or documents, ask questions related to the uploaded content, and receive AI-generated answers based on the information retrieved from the document.

The system retrieves relevant information from the uploaded PDF and generates context-based answers along with source page references.

Key Features

- Upload text-based PDF documents.
- Extract text from PDF files page by page.
- Split extracted text into smaller overlapping chunks.
- Generate text embeddings using Sentence Transformers.
- Store and search document embeddings using FAISS.
- Retrieve relevant document sections based on user questions.
- Generate answers using the Qwen2.5-3B-Instruct model.
- Display answers with source page references.
- Interactive chatbot-style interface using Gradio.
- Supports CPU execution when a GPU is unavailable.

Technologies Used

- Python – Core programming language.
- PyMuPDF – Extracts text and page information from PDF documents.
- Sentence Transformers – Generates text embeddings using "all-MiniLM-L6-v2".
- FAISS – Performs vector similarity search.
- Qwen2.5-3B-Instruct (GGUF) – Generates answers using a local language model.
- llama-cpp-python – Runs the quantized language model.
- Gradio – Creates the interactive user interface.
- Google Colab – Development and execution environment.

Project Workflow

1. PDF Upload: User uploads a text-based PDF document.
2. Text Extraction: PyMuPDF extracts text from each PDF page.
3. Text Chunking: Extracted text is divided into smaller overlapping chunks while preserving page metadata.
4. Embedding Generation: Sentence Transformers converts text chunks into numerical vectors.
5. Vector Indexing: FAISS stores the embeddings for efficient similarity searching.
6. Question Processing: The user's question is converted into an embedding.
7. Information Retrieval: FAISS retrieves the most relevant document chunks.
8. Answer Generation: Qwen2.5-3B-Instruct generates an answer using the retrieved document context.
9. Source References: Relevant source page numbers are included with the generated answer.
10. User Interface: Gradio provides an interactive interface for uploading PDFs and asking questions.

RAG Architecture

PDF Upload → Text Extraction → Text Chunking → Embeddings → FAISS Vector Search → Relevant Context Retrieval → Qwen2.5 LLM → Answer with Source Pages

How to Run

1. Open the project notebook in Google Colab.
2. Run the notebook cells sequentially from top to bottom.
3. Install the required Python libraries using the installation cells.
4. Load the embedding model and Qwen2.5 language model.
5. Launch the Gradio interface.
6. Upload a text-based PDF document.
7. Click on Process PDF.
8. Enter your question and click Ask Question.
9. View the generated answer with source page references.

Project Limitations

- Supports text-based PDFs with selectable text.
- Scanned or image-only PDFs are not supported because OCR is not implemented.
- Initial model downloads and loading may take time.
- CPU execution can be slower than GPU execution.
- AI-generated answers may occasionally contain errors, so source references should be verified.

Learning Outcomes

Through this project, I gained practical experience with:

- Generative AI and Large Language Models (LLMs).
- Retrieval-Augmented Generation (RAG).
- Text preprocessing and chunking.
- Text embeddings and semantic search.
- Vector databases and FAISS.
- Local open-source language models.
- Building interactive AI applications using Gradio.

Conclusion

This project demonstrates how Retrieval-Augmented Generation can be used to build an intelligent document question-answering system. It combines semantic search and a local Large Language Model to provide relevant, document-grounded answers with source references.
