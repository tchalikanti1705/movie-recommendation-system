# 🎬 Movie Recommendation System (Item-Based & Hybrid)

This project is a movie recommendation system built from scratch using the [MovieLens 10M Dataset](https://www.kaggle.com/datasets/amirmotefaker/movielens-10m-dataset-latest-version). It includes:

- ✅ **Item-Based Collaborative Filtering** — recommends similar movies based on user rating patterns.
- ✅ **Content-Based Filtering** — recommends movies based on genre similarity.
- ✅ **Hybrid Recommender System** — combines both methods for better accuracy.

---

## 📂 Dataset

**Source:** [MovieLens 10M Dataset](https://www.kaggle.com/datasets/amirmotefaker/movielens-10m-dataset-latest-version)

This dataset includes:
- `movies.dat`: Movie information including `movieId`, `title`, and `genres`.
- `ratings.dat`: User ratings including `userId`, `movieId`, `rating`, and `timestamp`.

---

## ⚙️ How It Works

### 1. 🧠 Collaborative Filtering (Item-Based)
- Create a **user-movie matrix** from the ratings data.
- Use **cosine similarity** to compare how users rated different movies.
- Recommend movies that were similarly rated by similar users.

### 2. 🎭 Content-Based Filtering
- Extract **genres** from the movie data.
- Use **TF-IDF vectorization** to convert genres into numerical vectors.
- Compute **genre-based cosine similarity** between movies.

### 3. 🤝 Hybrid Recommendation System
- Combine both approaches using a weighted average:
  
```python
hybrid_score = alpha * collaborative_score + (1 - alpha) * content_score
```


🚀 Future Enhancements
 Add a Streamlit web app for interactive recommendations
 Implement user login & preferences
 Enhance content-based filtering using metadata like actors, directors, and plot
 Add matrix factorization or deep learning-based models

