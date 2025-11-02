# RAG-News-QA-with-ChromaDB-and-OpenAI-
A minimal Retrieval-Augmented Generation pipeline in a single Jupyter Notebook. It loads .txt news articles, chunks them, embeds with OpenAI, stores in ChromaDB, retrieves relevant chunks, and answers questions concisely.
| Section | Content |
| --- | --- |
| Title | RAG News QA with ChromaDB and OpenAI (Notebook) |
| Description | A minimal Retrieval-Augmented Generation pipeline in a single Jupyter Notebook. It loads .txt news articles, chunks them, embeds with OpenAI, stores in ChromaDB, retrieves relevant chunks, and answers questions concisely. |
| Features | - Loads .txt files from news_articles. - Chunks text with overlap. - Uses OpenAI text-embedding-3-small for embeddings. - Stores and queries with Chroma persistent storage. - Generates concise answers using Chat Completions. |
| Prerequisites | - Python 3.9+ - OpenAI account and API key |
| Setup | 1) git clone  2) cd repo-root 3) python -m venv .venv && source .venv/bin/activate (Windows: .venv\Scripts\activate) 4) pip install -r requirements.txt 5) Create .env with OPENAI_API_KEY=sk-... |
| Data | Place .txt files in news_articles/. Each file becomes a document. Keep files small for demos. |
| Run the Notebook | 1) jupyter notebook (or VS Code) 2) Open notebooks/rag_news_qa.ipynb 3) Run cells in order 4) Edit the example question cell |
| Configuration | - Data directory: ./news_articles - Chroma path: ./chroma_persistent_storage - Embedding model: text-embedding-3-small - Chat model: gpt-3.5-turbo |
| Security | Do not commit your .env or API keys. .gitignore is configured to exclude secrets and local storage. |
| Troubleshooting | - If Chroma persists old data, delete chroma_persistent_storage/ locally. - Ensure OPENAI_API_KEY is set. - For Unicode issues, ensure encoding="utf-8". - For rate limits, add small sleeps between embedding calls. |
| License | Add a license (e.g., MIT) if you plan to share publicly. |
