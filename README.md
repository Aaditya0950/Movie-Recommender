# 🎬 Movie Recommender — A Smart Movie Suggestion App  

Movie Recommender is a **content-based recommendation app** built with Streamlit and trained on the TMDB Top 5000 Movies dataset. It suggests similar movies using **overview, genre, cast, crew, and keywords** through NLP and cosine similarity.  


## 🚀 Features  
- 🔍 Search by movie title  
- 🎯 Content-based recommendations (overview, genres, cast, director)  
- 🧠 TF-IDF vectorization + cosine similarity  
- 🖼️ Posters fetched live via TMDB API  
- 📱 Mobile-friendly UI with fuzzy search fallback  

## 📊 Dataset  
- **TMDB Top 5000 Movies**: ~5000 entries with rich metadata (overview, genres, keywords, cast, crew).  
- Two clean CSVs (`movies.csv`, `credits.csv`) merged via `id`.  
- Preprocessing: lowercased tokens, underscore-joined names → cleaner vector space & better similarity scores.  

## 🛠️ Tech Stack  
- Frontend: **Streamlit**  
- Backend: **Python, Pandas, Scikit-learn, Requests**  
- Data: **TMDB 5000 Movies Dataset (Kaggle)**  
- API: **TMDB API** for posters  
- Deployment: **Streamlit Community Cloud**  

## ⚡ Setup & Run  
```bash
# Clone repo
git clone https://github.com/yourusername/movierecommender.git
cd movierecommender

# Install dependencies
pip install -r requirements.txt

# Add TMDB API key
echo 'TMDB_API_KEY="your_api_key_here"' > .streamlit/secrets.toml

# Run app
streamlit run app.py
