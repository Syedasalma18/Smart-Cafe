# Smart-Cafe
Smart Café Assistant Chatbot| Python, React Native, RunPod, HugingFace, Firebase, Pinecone, LangChain • Built a multi-agent chatbot for a React Native café app, enabling real-time customer support and order handling. • Integrated a RAG pipeline with custom LLMs on RunPod to answer menu-related queries using LangChain and Pinecone

# ☕ Smart Café Assistant Chatbot

An intelligent, multi-agent café assistant powered by Retrieval-Augmented Generation (RAG), designed to handle real-time customer queries about orders, ingredients, allergens, and transaction history — integrated with Firebase for storing order data.

---

## 🧠 Project Description

This chatbot simulates a café assistant that answers questions based on actual transaction data from a CSV file. It uses advanced NLP techniques (RAG with LangChain + OpenAI or Hugging Face LLMs), Pinecone for semantic vector search, and Firebase to store customer order records.

---

## 🚀 Tech Stack

- **Python** (Colab-compatible)
- **LangChain** (LLM + RAG logic)
- **Pinecone** (Vector database)
- **OpenAI GPT / HuggingFace** (LLM inference)
- **Firebase Firestore** (Order storage)
- **Pandas** (CSV processing)
- **React Native** (Optional frontend integration)

---

## 📦 Features

- ☕ Answer customer queries like:
  - "Who served Hot Chocolate?"
  - "How much is an Iced Tea?"
  - "Which payment method was used for Espresso?"
- 🔍 Vector-based semantic retrieval from CSV data
- 🗂️ Data embedded into Pinecone for scalable search
- 💬 Uses OpenAI or custom LLMs hosted on RunPod
- 🔐 Firebase integration for order storage

---

## 📁 Dataset

The chatbot is powered by a real café transactional dataset in CSV format:

| Item          | Size  | Price | Gender | Payment Method | Staff | ... |
|---------------|-------|-------|--------|----------------|-------|-----|

---

## 🛠️ Setup Instructions

### 🔹 1. Clone the Repo

```bash
git clone https://github.com/your-username/smart-cafe-assistant.git
cd smart-cafe-assistant
```

### 🔹 2. Install Dependencies (For local)

```bash
pip install -r requirements.txt
```

For Google Colab, run:
```python
!pip install -U langchain langchain-community openai pinecone-client firebase-admin
```

### 🔹 3. Add Your API Keys

Create a file named `.env` or directly in code:

```python
OPENAI_API_KEY = "sk-XXXX"
PINECONE_API_KEY = "your-pinecone-key"
PINECONE_ENV = "your-environment"
```

Upload your Firebase Admin SDK JSON key in Colab:
```python
from google.colab import files
uploaded = files.upload()
```

---

## 🔍 Example Usage

```python
query = "Who served Americano?"
result = qa_chain({"query": query})
print("Answer:", result["result"])
```

```python
# Save order to Firebase
order = {
  "item": "Espresso",
  "price": 5.20,
  "user": "Syeda",
  "time": firestore.SERVER_TIMESTAMP
}
db.collection("orders").add(order)
```

---

## 💡 Future Scope

- 🔄 Live integration with React Native café app
- 📲 WhatsApp chatbot version
- 📊 Analytics dashboard (Power BI or Streamlit)
- 🔐 Role-based admin access

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

## 📜 License

MIT License © 2025 Syeda Salma Syed Arif
