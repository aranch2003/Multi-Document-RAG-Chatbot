# Multi-Document RAG Chatbot 🤖

A Streamlit web application that allows you to chat with multiple PDF documents at once using Google's Gemini Pro model. This project implements a Retrieval-Augmented Generation (RAG) pipeline to provide answers based on the content of the uploaded files.

---

## 📘 About The Project

This application serves as a powerful interface to query information from a collection of PDF documents. Users can upload multiple PDFs, which are then processed, chunked, and stored in a FAISS vector store. The app then uses a conversational chain powered by LangChain and the Gemini API to answer user questions based on the retrieved context from the documents.

### ✨ Features

- **Multi-Document Upload:** Upload one or more PDF files simultaneously.
- **Text Processing:** Automatically extracts and chunks text from the uploaded documents.
- **Vector Store Creation:** Creates an in-memory FAISS vector index for efficient similarity searches.
- **Conversational AI:** Uses LangChain and Google Gemini to hold a conversation based on the document's context.
- **User-Friendly Interface:** A clean and simple UI built with Streamlit.

### 🧰 Tech Stack

- **Frontend:** Streamlit
- **LLM Framework:** LangChain
- **AI Model:** Google Gemini
- **Vector Store:** FAISS (Facebook AI Similarity Search)
- **PDF Processing:** PyPDF2

---

## 🚀 Project Setup: From Zero to Running App

These instructions will get you a copy of the project up and running on your local machine.

### ✅ Prerequisites

- Python 3.8 or higher
- Git installed

### 🔧 Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 🏗️ Step 2: Create and Activate a Virtual Environment

```bash
# Windows
python -m venv myenv
.\myenv\Scripts\activate

# macOS/Linux
python3 -m venv myenv
source myenv/bin/activate
```

### 📦 Step 3: Install Dependencies

Install all the required libraries from the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

> 💡 Tip: If the `requirements.txt` file is missing or outdated, you can regenerate it using `pip freeze > requirements.txt`.

### 🔐 Step 4: Set Up Your API Key

Create a `.env` file in the root of your project:

```
GOOGLE_API_KEY="your_actual_api_key_here"
```

> ⚠️ **Do not commit your `.env` file** to version control or share it publicly.

### ▶️ Step 5: Run the Application

```bash
streamlit run main.py
```

---

## ☁️ Deploy to Streamlit Community Cloud

To make your app accessible online:

1. **Push to GitHub**  
   Ensure your code and `requirements.txt` file are committed and pushed.

2. **Sign in to Streamlit Cloud**  
   Go to [https://share.streamlit.io](https://share.streamlit.io) and sign in with GitHub.

3. **Create a New App**
   - Click **"New app"**
   - Select your repository and branch
   - Set the **main file path** to `main.py`

4. **Add Secrets**
   - In **Advanced settings**, add your API key like this:
     ```
     GOOGLE_API_KEY="your_actual_api_key_here"
     ```

5. **Deploy!**  
   Click **Deploy** and your app will be live within seconds 🎉

---

## 🔄 Updating the Repository (Including This README)

To update your code or add this `README.md`:

1. **Stage Your Changes**
   ```bash
   git add .
   ```

2. **Commit Your Changes**
   ```bash
   git commit -m "Add comprehensive README file"
   ```

3. **Push to GitHub**
   ```bash
   git push
   ```

---

## ⚠️ Known Limitations

> This is currently a demonstration version. Keep these limitations in mind:

- **Stateless Sessions:**  
  The FAISS vector store is created in-memory. When the app restarts, uploaded files and vectors are lost.

- **Single-User Focus:**  
  The app is not yet multi-user capable. It does not store chat history or sessions across users or time.

---


---

## 🙋‍♂️ Questions or Contributions?

Feel free to open an issue or submit a pull request. Contributions are welcome!

