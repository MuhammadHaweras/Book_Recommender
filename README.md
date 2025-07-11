# 📚 LLM-Based Semantic Book Recommender System

> ⚠️ **Note on Deployment**  
> Due to limited OpenAI API credits, I have **not provided a live Hugging Face demo link** for this project.  
> 
> While the app is fully functional and tested, real-time queries depend on OpenAI's paid API access.  
> 
> If you'd like to try it out locally, you're welcome to clone the repo and add your own OpenAI API key.
> 
> Your understanding and cooperation are deeply appreciated. 🙏 Just trust me that I have deployed on huggingface spaces 😅


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
git clone https://github.com/MuhammadHaweras/Book_Recommendor.git
cd book_recommendor

pip install -r requirements.txt

Add OpenAI Key (Create a .env file)

Run the App
python app.py

🏷️ Tags
#LangChain #LLM #BookRecommender #Gradio #OpenAI #ChromaDB #EmotionClassification #HuggingFaceSpaces


