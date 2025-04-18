RAG-LangChain Implementation 🔍
A simple implementation of Retrieval Augmented Generation using LangChain and Hugging Face models.
Overview 📋
This Jupyter notebook demonstrates how to build a question-answering system that uses local documents as context. The implementation:

Loads markdown documents from a local directory
Splits documents into manageable chunks
Creates embeddings using Hugging Face's all-MiniLM-L6-v2 model
Stores vectors in a FAISS index for efficient retrieval
Processes questions using a retrieval pipeline with Flan-T5-Large

Requirements 🛠️
langchain
langchain_text_splitters
langchain_community
huggingface_hub
transformers
python-dotenv
faiss-cpu
Usage 💻

Place your markdown documents in a ./docs directory
Set up your Hugging Face token in a .env file
Run the notebook cells sequentially
Use the qa_chain.invoke() method to ask questions about your documents

Example Queries 💬
The notebook demonstrates querying personal information from the loaded documents:

"When was I suffered Migraine?"
"Which cities I'm visiting in Japan"
"What's my interests"

Performance Notes 📊
The notebook uses Flan-T5-Large for generation, which runs on CPU by default. Consider using a GPU for better performance with larger documents.
