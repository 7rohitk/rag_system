📊 RAG-Based Financial QA System
---
An intelligent Retrieval-Augmented Generation (RAG) application built using LangChain, Groq (LLaMA 3), FAISS, and Gradio to extract and answer financial questions from Amazon’s Q3 2024 10-Q SEC filing PDF.

---
🚀 Features
🔍 Automatically converts 10-Q PDF into markdown using Docling <br>
📄 Splits documents based on markdown headers for better chunking<br>
🧠 Creates semantic embeddings using HuggingFace Transformers<br>
📁 Stores and indexes embeddings in FAISS for fast retrieval<br>
🧑‍💻 Uses Groq LLaMA3-8B for fast, contextual answer generation<br>
💬 Interactive Q&A interface using Gradio<br>
✅ Streams answers to maintain LLM performance and UX<br>

---
🧰 Tech Stack

LLM	LLaMA 3 (via Groq API)<br>
Embeddings	sentence-transformers/all-MiniLM-L6-v2<br>
Vector Store	FAISS<br>
PDF → Markdown	Docling<br>
LangChain Modules	RAG Chain, Prompt Template, Retriever, etc.<br>
Interface	Gradio UI<br>

---
📂 Project Structure
 
├── amazon-10-q-q3-2024.pdf     # Sample input file<br>
├── app.py                      # Main code<br>
├── README.md                   # Project documentation<br>

---
⚙️ How to Run
Install dependencies<br>
pip install langchain langchain-community langchain-core langchain-groq faiss-cpu sentence-transformers docling gradio<br>
Set Groq API Key<br>
import os<br>
os.environ["GROQ_API_KEY"] = "your_api_key_here"<br>
Run the app<br>
python app.py<br>
This will launch a Gradio interface where you can upload a PDF and ask questions.<br>

---

💻 Gradio Demo
Upload PDF	Ask Financial Questions	Get Streamed Answers<br>
✅ Yes	✅ Yes	✅ Yes<br>

Example questions:<br>

What was Amazon’s net income in Q3 2024?<br>

How does Q3 2024 revenue compare to Q3 2023?<br>

What are the main operating expense categories?<br>

 
🧠 Sample RAG Answer
 
Question: What was the net income for Q3 2024?<br>
• The net income for Q3 2024 was $15,328 million.<br>
• Compared year over year, the net income increased from $9,879 million in Q3 2023.<br>
