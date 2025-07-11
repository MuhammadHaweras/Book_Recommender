# 📚 LLM-Based Semantic Book Recommender System

> **Live Demo**: [🌐 View on Hugging Face Spaces](https://huggingface.co/spaces/haweras/llm_book_recommendor)

A semantic book recommendation system that uses **Large Language Models**, **OpenAI embeddings**, and **LangChain** to deliver personalized book suggestions based on your input description, emotional tone, and category.

---

## 🧠 Key Features

- 🔍 **Semantic Search** using OpenAI Embeddings and ChromaDB
- ❤️ Emotion-aware recommendations powered by a fine-tuned emotion classifier
- 🧾 Category mapping to simplify complex metadata
- 🖼️ Interactive Gradio dashboard with thumbnails & smart captions
- ☁️ Hosted on Hugging Face Spaces for free & public access

---

## 🗂️ Project Structure

📦 book_recommendor
├── app.py # Gradio app entry point (main dashboard)
├── books_with_emotions.csv # Enriched book metadata with emotions
├── tagged_description.txt # Raw text for Chroma vector store
├── cover-not-found.jpg # Default image if book thumbnail is missing
├── requirements.txt # Python dependencies
└── README.md # Project documentation


---

## 🛠️ How It Works

1. **Vector Embedding**: `tagged_description.txt` is processed with `OpenAIEmbeddings` to create a vector store using `Chroma`.
2. **Query Input**: User inputs a sentence like `"A heartwarming story about forgiveness"`.
3. **Similarity Search**: Top matching books are retrieved semantically.
4. **Tone & Category Filter**: Filters results based on emotional tone and book category.
5. **Output Display**: Shows book cover, author(s), and a short summary using Gradio.

---

## 🤖 ML & NLP Components

- **Text Embedding**: `langchain_openai.OpenAIEmbeddings`
- **Vector Search**: `Chroma` from `langchain.vectorstores`
- **Emotion Detection**: `j-hartmann/emotion-english-distilroberta-base` via Hugging Face Transformers
- **Frontend UI**: Gradio with dropdown filters for category and tone

---

## 📦 Setup & Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com/MuhammadHaweras/book_recommendor.git
cd book_recommendor

pip install -r requirements.txt

Add OpenAI Key (Create a .env file)

Run the App
python app.py

 Deployment
This project is live and publicly hosted at:
🔗 https://huggingface.co/spaces/haweras/llm_book_recommendor

🏷️ Tags
#LangChain #LLM #BookRecommender #Gradio #OpenAI #ChromaDB #EmotionClassification #HuggingFaceSpaces


