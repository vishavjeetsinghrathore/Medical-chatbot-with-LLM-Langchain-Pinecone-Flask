# 🩺 Medical Chatbot with LLM, LangChain, Pinecone & Flask

An AI-powered Medical Chatbot built using **Google Gemini 2.5 Flash**, **LangChain**, **Pinecone Vector Database**, **Hugging Face Embeddings**, and **Flask**.

The chatbot uses Retrieval-Augmented Generation (RAG) to answer medical-related questions based on the contents of a medical PDF stored in a Pinecone vector database.

---

## 🚀 Features

* Medical Question Answering using RAG
* Google Gemini 2.5 Flash as the Large Language Model
* Hugging Face Sentence Transformer Embeddings
* Pinecone Vector Database for semantic search
* PDF ingestion and indexing
* Flask-based web interface
* LangChain Retrieval Chain
* Clean and modular project structure

---

## 🛠️ Tech Stack

* Python
* Flask
* LangChain
* Google Gemini 2.5 Flash
* Hugging Face Sentence Transformers
* Pinecone
* PyPDF
* HTML, CSS, JavaScript

---

## 📂 Project Structure

```text
Medical-chatbot/
│
├── app.py
├── store_index.py
├── requirements.txt
├── .env
│
├── data/
│   └── medical_book.pdf
│
├── src/
│   ├── helper.py
│   └── prompt.py
│
├── templates/
│   └── chat.html
│
└── static/
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd Medical-chatbot
```

---

### 2. Create Virtual Environment

Windows

```bash
python -m venv .venv
```

Activate

```bash
.venv\Scripts\activate
```

Linux / macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
PINECONE_API_KEY=your_pinecone_api_key
GEMINI_API_KEY=your_gemini_api_key
```

---

## 📄 Add Medical Data

Place your medical PDF inside the `data/` folder.

Example:

```text
data/
└── medical_book.pdf
```

---

## 🧠 Create Pinecone Index

Create a Pinecone index with the following configuration:

| Setting    | Value           |
| ---------- | --------------- |
| Index Name | medical-chatbot |
| Dimension  | 384             |
| Metric     | Cosine          |

> **Note:** The project uses the Hugging Face model `sentence-transformers/all-MiniLM-L6-v2`, which generates **384-dimensional embeddings**.

---

## 📥 Store Embeddings in Pinecone

Run:

```bash
python store_index.py
```

This will:

* Load the medical PDF
* Split the document into chunks
* Generate embeddings
* Store vectors in Pinecone

---

## ▶️ Run the Application

```bash
python app.py
```

Flask server starts at:

```text
http://127.0.0.1:8080
```

Open the URL in your browser.

---

## 💬 Example Questions

* What is diabetes?
* What are the symptoms of malaria?
* What causes hypertension?
* Explain asthma.
* What is pneumonia?

---

## 🔄 Application Workflow

```text
User
   │
   ▼
Flask Web App
   │
   ▼
LangChain Retriever
   │
   ▼
Pinecone Vector Database
   │
Retrieve Relevant Medical Chunks
   │
   ▼
Gemini 2.5 Flash
   │
Generate Answer
   │
   ▼
Flask
   │
   ▼
Browser
```

---

## 📦 Main Dependencies

* Flask
* LangChain
* LangChain Community
* LangChain Google GenAI
* LangChain Pinecone
* Hugging Face Sentence Transformers
* Pinecone
* PyPDF
* Python Dotenv

---

## 📌 Future Improvements

* Conversation Memory
* Chat History
* Source Citations
* Streaming Responses
* Docker Support
* Authentication
* Multi-PDF Knowledge Base
* Deployment on Render or AWS

---

## 👨‍💻 Author

**Vishavjeet Singh**

B.Tech | Full Stack Developer | AI & Generative AI Enthusiast

---

## 📄 License

This project is developed for educational and learning purposes.
