# 📄 PDF Chatbot (RAG using Gemini + TF-IDF)

A simple AI-powered chatbot that allows users to ask questions from a PDF file.  
It uses TF-IDF + cosine similarity for retrieval and Google Gemini API for generating answers.

---

## 🚀 Features

- 📄 PDF text extraction using PyPDF2  
- ✂️ Smart chunking with overlap for better context  
- 🔍 TF-IDF + cosine similarity retrieval system  
- 🤖 Google Gemini AI for response generation  
- 💬 Streamlit web interface  
- 📌 Shows retrieved context for transparency  

---

## 🛠️ Tech Stack

- Python  
- Streamlit  
- Google Generative AI (Gemini)  
- scikit-learn  
- PyPDF2  
- python-dotenv  
- pickle  

---

## 📁 Project Structure

```
PDF-Chatbot/
│
├── app.py                # Streamlit chatbot app
├── preprocess.py         # PDF → text → chunk generator
├── chunks.pkl            # Saved text chunks
├── Recipe-Book.pdf       # Input PDF file
├── .env                  # API key file
└── README.md
```

---

## ⚙️ Installation

### Clone the repository
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### Create virtual environment (optional)
```bash
python -m venv venv
venv\Scripts\activate   # Windows
# source venv/bin/activate  # Mac/Linux
```

### Install dependencies
```bash
pip install streamlit google-genai scikit-learn python-dotenv PyPDF2
```

---

## 🔑 Setup .env file

Create a `.env` file in the root folder:

```
GOOGLE_API_KEY=your_google_gemini_api_key_here
```

---

## ▶️ How to Run

### Step 1: Generate chunks
```bash
python preprocess.py
```

### Step 2: Run app
```bash
streamlit run app.py
```

---

## 🧠 How It Works

- PDF is loaded and text is extracted  
- Text is split into overlapping chunks  
- TF-IDF converts chunks into vectors  
- User question is vectorized  
- Cosine similarity finds relevant chunks  
- Context is sent to Gemini API  
- Gemini generates final answer  

---

## 📌 Example Questions

- What is this document about?  
- What ingredients are mentioned?  
- How do I prepare the recipe?  
- What steps are listed in the PDF?  

---

## ⚠️ Limitations

- Works only with text-based PDFs (not scanned images)  
- Accuracy depends on chunking and TF-IDF retrieval  
- Requires internet connection for Gemini API  

---

## 🔮 Future Improvements

- Add FAISS / vector database for better search  
- Allow user PDF upload in UI  
- Support multiple PDFs  
- Add voice input/output  
- Deploy on Streamlit Cloud  

---

## 👩‍💻 Author

Made with ❤️ by Jesna Jaison
