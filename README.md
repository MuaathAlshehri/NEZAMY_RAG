# ⚖️ Saudi Labor Law RAG System 

An advanced Retrieval-Augmented Generation (RAG) pipeline built to navigate, search, and query the Saudi Labor Law. 

## Features
- **Custom OCR Pipeline:** Extracts text from Arabic PDFs using PyMuPDF and Tesseract.
- **Hierarchical Semantic Chunking:** Custom text splitter that intelligently chunks legal text by `[Chapter] -> [Section] -> [Article]` preserving full legal context.
- **Hybrid Search Engine:** Combines semantic dense retrieval (HuggingFace `e5-base`) with exact keyword matching (BM25) to mitigate Arabic OCR typos.
- **LLM Integration:** Powered by Google's `gemini-2.5-flash` with strict hallucination guardrails (Temperature = 0).
- **Interactive UI:** Built with Gradio, featuring both an AI Assistant and a Direct Vector Search Engine.

## Tech Stack
- **LangChain** (ChromaDB, Prompt Templates, Retrievers)
- **HuggingFace** (Embeddings)
- **Google Generative AI** (Gemini)
- **Gradio** (Frontend UI)
- **Tesseract OCR** (Data Extraction)

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Set your Google API Key: `export GOOGLE_API_KEY="your_api_key_here"`
3. Build the Vector Database: `data_pipeline.ipynb`
4. Run the App: `test.ipynb`


## ⚙️ How to Run Locally
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/MuaathAlshehri/NEZAMY_RAG.git](https://github.com/MuaathAlshehri/NEZAMY_RAG.git)
   cd NEZAMY_RAG