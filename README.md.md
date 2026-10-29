# PDF RAG Question Answering

## Overview

This project implements a basic Retrieval-Augmented Generation (RAG) pipeline that answers questions using information retrieved from PDF documents.

Instead of relying only on the language model's existing knowledge, the system retrieves relevant document chunks and provides them as context to the model.

## Features

- Load PDF documents using PyPDFLoader.
- Split documents into smaller chunks.
- Generate embeddings using Sentence Transformers.
- Store and search embeddings using FAISS.
- Retrieve relevant document chunks for user questions.
- Generate answers using the FLAN-T5 language model.
- Ask questions interactively about the PDF.

## Technologies Used

- Python
- Google Colab
- LangChain
- PyPDF
- Sentence Transformers
- FAISS
- Hugging Face Transformers
- FLAN-T5

## RAG Workflow

1. Load the PDF document.
2. Split the document into chunks.
3. Generate embeddings for each chunk.
4. Store the embeddings in FAISS.
5. Convert the user's question into an embedding.
6. Retrieve relevant document chunks.
7. Combine the retrieved context with the question.
8. Generate an answer using FLAN-T5.

## Installation

Install the required libraries:

```bash
pip install -r requirements.txt
```

## How to Run

1. Open `rag_pdf_qa.ipynb` in Google Colab.
2. Install the required libraries.
3. Load the sample PDF.
4. Run the notebook cells in order.
5. Enter a question about the PDF.
6. View the generated answer.

## Example

**Question:** How many days of annual leave do full-time employees receive?

**Context:** Full-time employees receive 20 days of paid annual leave per calendar year.

**Expected answer:** Full-time employees receive 20 days of paid annual leave per calendar year.

## Limitations

- Answer quality depends on the retrieved context.
- The model may generate incorrect answers or hallucinate.
- Retrieval may return irrelevant chunks.
- This is an educational project and should not be used for critical decisions without further validation.

## Future Improvements

- Support multiple PDF documents.
- Improve retrieval quality.
- Add source citations to answers.
- Build a web interface using Streamlit.
- Evaluate retrieval and answer quality.

## Disclaimer

The sample company policy document is fictional and is used for educational purposes only.
