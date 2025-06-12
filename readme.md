# RAG Tutorial Project

This project demonstrates a simple Retrieval-Augmented Generation (RAG) pipeline using OpenAI, ChromaDB, and LangChain. It is designed to ingest and query documents (such as PDFs) using modern LLM and vector database tools.

## Features

- Ingests PDF documents and stores their embeddings in a local ChromaDB instance.
- Uses OpenAI's API for embedding and language model tasks.
- Provides scripts for database population and question answering.

## Project Structure

```
.env
.gitignore
ask.py
fill_db.py
requirements.txt
chroma_db/
    chroma.sqlite3
    ...
data/
    gardening.pdf
```

- **.env**: Stores your OpenAI API key.
- **ask.py**: Script to query the knowledge base using natural language.
- **fill_db.py**: Script to ingest documents and populate the ChromaDB vector store.
- **requirements.txt**: Python dependencies.
- **chroma_db/**: Contains the ChromaDB SQLite database and related files.
- **data/**: Directory for source documents (e.g., PDFs).

## Setup

1. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

2. **Set your OpenAI API key:**
   - Edit `.env` and set `OPENAI_API_KEY` to your OpenAI key.

3. **Add documents:**
   - Place your PDF files in the `data/` directory.

4. **Ingest documents:**
   ```sh
   python fill_db.py
   ```

5. **Ask questions:**
   ```sh
   python ask.py
   ```

## Requirements

- Python 3.8+
- See [requirements.txt](requirements.txt) for Python packages.

## Notes

- This project uses [ChromaDB](https://www.trychroma.com/) for local vector storage.
- [LangChain](https://python.langchain.com/) is used for document processing and LLM integration.
- [OpenAI](https://platform.openai.com/) provides embeddings and language model responses.

## License

This project is for educational purposes.