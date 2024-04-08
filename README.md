# Chat with PDF Locally using Ollama + LangChain

A powerful local Retrieval Augmented Generation (RAG) application enabling you to interactively chat with your PDF documents using Ollama and LangChain. This application includes a Streamlit web interface and a Jupyter notebook for experimentation.

## Features

- 🔒 **Fully local processing** – your data never leaves your machine.
- 📄 **Intelligent PDF processing** with effective document chunking.
- 🧠 **Multi-query retrieval** for enhanced context understanding.
- 🎯 **Advanced RAG implementation** leveraging LangChain.
- 🖥️ **User-friendly Streamlit interface** for easy interaction.
- 📓 **Jupyter notebook** included for experimentation and development.

## 🚀 Quick Start

### 1. Prerequisites

- **Install Ollama** from [Ollama's official website](https://ollama.ai)
- Pull required models:

```bash
ollama pull llama3.2
ollama pull nomic-embed-text
```

### 2. Clone Repository

```bash
git clone "repo name"
cd ollama_pdf_rag
```

### 3. Set Up Environment

```bash
python -m venv venv
source venv/bin/activate  # Windows: .\venv\Scripts\activate
pip install -r requirements.txt
```

**Key dependencies:**

```
ollama==0.4.4
streamlit==1.40.0
pdfplumber==0.11.4
langchain==0.1.20
langchain-core==0.1.53
langchain-ollama==0.0.2
chromadb==0.4.22
```

### 🎮 Running the Application

**Streamlit Web Interface:**

```bash
python run.py
```
- Open your browser at [`http://localhost:8501`](http://localhost:8501).

**Jupyter Notebook for Experiments:**

```bash
jupyter notebook
```
- Open the notebook `updated_rag_notebook.ipynb` to start experimenting.

## 💡 Usage Tips

- **Upload PDFs** directly from the Streamlit interface.
- **Select different Ollama models** based on your preference.
- **Interact via chat** with uploaded PDFs seamlessly.
- Adjust the PDF viewer with the **zoom slider**.
- Clean your workspace by clicking the **"Delete Collection" button** when changing PDFs.

## ⚠️ Troubleshooting

- Ensure **Ollama** is running and models are downloaded.
- Verify Python environment activation.

### Common Errors

#### ONNX DLL Error

If encountering DLL errors:

1. Install Microsoft Visual C++ Redistributable:
   - [Download Link](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)
   - Install both x64 and x86 versions, then restart your computer.

2. If issues persist:

```bash
pip uninstall onnxruntime onnxruntime-gpu
pip install onnxruntime
```

#### CPU-Only Systems

For CPU-only users:

```bash
pip uninstall onnxruntime-gpu
pip install onnxruntime
```

- Adjust chunk size if memory issues occur (recommended 500-1000).

---

