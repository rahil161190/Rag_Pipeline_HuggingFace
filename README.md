# 📘 RAG Pipeline – Hugging Face

## 🚀 Demo Video

🎥 [Click here to watch the demo](https://rahil161190.github.io/Rag_Pipeline_HuggingFace/?utm_source=copilot.com)

<video src="demo.mp4" controls width="600"></video>

## ⭐ Situation
Retrieval-Augmented Generation (RAG) combines **retrieval of relevant documents** with **generation from large language models (LLMs)**.  
This project demonstrates how to build a practical RAG pipeline using Hugging Face datasets, sentence-transformer embeddings, and ChromaDB as the vector store.

---

## 🎯 Task
The goal of this project is to:
- Load Hugging Face documentation dataset (`m-ric/huggingface_doc`).
- Preprocess and chunk documents for efficient retrieval.
- Generate embeddings using `all-MiniLM-L6-v2`.
- Store embeddings in **ChromaDB** for semantic search.
- Query the system with natural language and retrieve relevant context for LLMs.

---

## ⚙️ Action
Steps implemented in this project:

1. **Dataset Loading**  
   - Hugging Face documentation dataset with 2,647 documents.  
   - Features: `text`, `source`.

2. **Chunking Strategy**  
   - Used `chonkie` with GPT-2 tokenizer.  
   - Fixed-size token chunking (128–256 tokens).  
   - Overlap of 32 tokens for better context preservation.

3. **Embedding Generation**  
   - SentenceTransformer model: `all-MiniLM-L6-v2`.  
   - Embedding dimension: 384.  
   - Generated embeddings for **33,769 chunks**.

4. **Vector Store (ChromaDB)**  
   - Created collection `huggingface_docs`.  
   - Added all chunks in batches of 5,000.  
   - Final count: **33,769 documents indexed**.

5. **Querying**  
   - Example query: *“How do I load a pretrained model?”*  
   - Embedding generated and compared against stored vectors.  
   - Retrieved semantically relevant documentation chunks.

---

## 📊 Result
- Successfully built a **scalable RAG pipeline**.  
- Enables **semantic search** across Hugging Face documentation.  
- Provides **context-aware answers** by combining retrieval + generation.  
- Demonstrates practical use of embeddings, chunking, and vector databases.
- Deployed as a **Gradio app** for interactive use.  

---



---

## 🛠️ Tech Stack
- **Python 3.12**
- **Hugging Face Datasets & Tokenizers**
- **SentenceTransformers (all-MiniLM-L6-v2)**
- **Chonkie (chunking + visualization)**
- **ChromaDB (vector store)**
- **Google GenAI (Gemini API client)**

---

## 📌 Next Steps
- Integrate with **LangChain** for agentic workflows.  
- Add **evaluation metrics** for retrieval quality.  


