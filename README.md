**🤖 Multimodal PDF Question Answering System (RAG + LangChain + Gradio)**

This project is a multimodal Retrieval-Augmented Generation (RAG) pipeline for querying PDF documents that may contain text, images, and tables.
It integrates LangChain, OpenAI LLMs, and Gradio to provide an interactive interface where users can upload PDFs and ask natural language questions — and the system retrieves and reasons over multiple modalities (text + images + tables).

**🚀 Features**

**📄 Text Understanding** – Extracts and chunks text using LangChain.

**🖼️ Image Extraction** – Extracts images and allows reference in answers.

**📊 Table Extraction** – Converts detected tables into structured Pandas DataFrames.

**🔍 Vector Search with Query Expansion** – Embeds text into FAISS and enhances queries for improved retrieval accuracy.

**🧠 Retrieval-Augmented Generation (RAG)** – Uses LLMs with contextual grounding from text + metadata (images & tables).

**🎛️ Interactive UI** – Powered by Gradio for uploading PDFs and asking questions in real time.

**🛠️ Tech Stack**

Python 3.10+

LangChain (chains, prompts, embeddings, RAG pipeline)

OpenAI API (ChatOpenAI + Embeddings)

FAISS (Vector Database)

PyMuPDF (fitz) – Image & table extraction

PyPDF2 – Text extraction

Pytesseract – OCR support for scanned images

Pandas – Table structuring

Gradio – Frontend interface



**⚙️ Setup Instructions**

1️⃣ Clone the Repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

**2️⃣ Create Virtual Environment & Install Dependencies**
python -m venv venv
source venv/bin/activate   # For Linux/Mac
venv\Scripts\activate      # For Windows

pip install -r requirements.txt

**3️⃣ Configure Environment Variables**

Create a .env file in the project root:

OPENAI_API_KEY=your_api_key_here

**▶️ Run the Application**
python project.py


**The app will start at:**
👉 http://127.0.0.1:7860

**💻 Usage**

Upload a PDF file (supports text, images, and tables)

Enter your question in natural language

The system will:

Expand your query with related terms

Retrieve relevant text chunks and metadata about images/tables

Generate a concise, multimodal-aware answer using the LLM

View the answer and processing logs in real time

**📊 Example**

Upload PDF: Research paper with figures & tables

Question: "What does Table 2 indicate about accuracy?"

Answer: Refers directly to Table 2 in the PDF with summarized insights

Log: Shows query expansion, retrieved chunks, and multimodal references
