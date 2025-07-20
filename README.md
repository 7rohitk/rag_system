📊 RAG-Based Financial QA System
An intelligent Retrieval-Augmented Generation (RAG) application built using LangChain, Groq (LLaMA 3), FAISS, and Gradio to extract and answer financial questions from Amazon’s Q3 2024 10-Q SEC filing PDF.

🚀 Features
🔍 Automatically converts 10-Q PDF into markdown using Docling

📄 Splits documents based on markdown headers for better chunking

🧠 Creates semantic embeddings using HuggingFace Transformers

📁 Stores and indexes embeddings in FAISS for fast retrieval

🧑‍💻 Uses Groq LLaMA3-8B for fast, contextual answer generation

💬 Interactive Q&A interface using Gradio

✅ Streams answers to maintain LLM performance and UX

🧰 Tech Stack
Component	Tech Used
LLM	LLaMA 3 (via Groq API)
Embeddings	sentence-transformers/all-MiniLM-L6-v2
Vector Store	FAISS
PDF → Markdown	Docling
LangChain Modules	RAG Chain, Prompt Template, Retriever, etc.
Interface	Gradio UI

📂 Project Structure
css
Copy
Edit
├── amazon-10-q-q3-2024.pdf     # Sample input file
├── app.py                      # Main code
├── README.md                   # Project documentation
⚙️ How to Run
Install dependencies


pip install langchain langchain-community langchain-core langchain-groq faiss-cpu sentence-transformers docling gradio
Set Groq API Key

import os
os.environ["GROQ_API_KEY"] = "your_api_key_here"
Run the app
python app.py
This will launch a Gradio interface where you can upload a PDF and ask questions.

💻 Gradio Demo
Upload PDF	Ask Financial Questions	Get Streamed Answers
✅ Yes	✅ Yes	✅ Yes

Example questions:

What was Amazon’s net income in Q3 2024?

How does Q3 2024 revenue compare to Q3 2023?

What are the main operating expense categories?

 
🧠 Sample RAG Answer
 
Question: What was the net income for Q3 2024?
• The net income for Q3 2024 was $15,328 million.
• Compared year over year, the net income increased from $9,879 million in Q3 2023.
