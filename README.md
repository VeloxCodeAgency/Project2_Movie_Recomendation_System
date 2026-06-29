# 🎬 Movie Recommendation System
### VeloxCode Agency Internship | ML Project 2

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat&logo=scikit-learn)
![Google Colab](https://img.shields.io/badge/Google-Colab-yellow?style=flat&logo=googlecolab)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## 🎯 What is this project?

Ever wondered how **Netflix knows exactly what you want to watch next?**  
This project demystifies that magic by building a **Movie Recommendation Engine** from scratch using two powerful approaches — Content-Based Filtering and Collaborative Filtering — just like real streaming platforms use under the hood.

---

## 🗂️ Dataset Overview

### Movies Dataset
| Feature | Description |
|---------|-------------|
| `movie_id` | Unique identifier |
| `title` | Movie name |
| `genres` | Action / Drama / Horror / Romance etc. |
| `director` | Director name |
| `rating` | IMDb-style rating (1-10) |

### Ratings Dataset
- **10 users × 20 movies** User-Item Matrix
- Ratings scale: 1 (poor) to 5 (excellent)
- Realistic sparsity (~60% rated per user)

---

## 🔍 Project Workflow

```
Movies + Ratings Data → EDA → Content-Based → Collaborative → Hybrid → Evaluation
```

### 1️⃣ Exploratory Data Analysis
- Movie rating distribution
- Genre frequency analysis
- User-Item matrix sparsity heatmap

### 2️⃣ Content-Based Filtering
Uses **what the movie is about** to find similar movies

```
Movie Features (genres + director)
        ↓
   TF-IDF Vectorization
        ↓
  Cosine Similarity Matrix
        ↓
  Top-N Similar Movies
```

### 3️⃣ Collaborative Filtering
Uses **what similar users liked** to make recommendations

```
User Ratings History
        ↓
  Pearson Correlation
        ↓
  Find Similar Users
        ↓
  Recommend Their Top Movies
```

### 4️⃣ Hybrid System
Combines **both approaches** for best accuracy — exactly how Netflix works!

---

## 📐 Similarity Metrics Explained

| Metric | Used In | How It Works |
|--------|---------|--------------|
| **Cosine Similarity** | Content-Based | Measures angle between feature vectors (0=different, 1=identical) |
| **Pearson Correlation** | Collaborative | Measures linear relationship between user rating patterns (-1 to +1) |

---

## 🏆 Sample Output

```
🎬 "You liked Inception? You might also enjoy:"
  1. Interstellar        (Similarity: 0.91)
  2. The Dark Knight     (Similarity: 0.87)
  3. The Matrix          (Similarity: 0.74)
  4. Avengers Endgame    (Similarity: 0.61)
  5. Get Out             (Similarity: 0.42)
```

---

## 📊 Evaluation

- **Precision@K** metric used to evaluate recommendation quality
- Measures: *"Of the top-K recommendations, how many did the user actually like?"*

---

## 🛠️ Tech Stack

- **Language:** Python 3.8+
- **Libraries:** Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn
- **Techniques:** TF-IDF, Cosine Similarity, Pearson Correlation
- **Environment:** Google Colab

---

## 💡 Key Learnings

- Content-Based filtering works even without user history (solves Cold Start)
- Collaborative Filtering captures hidden user preferences that content alone misses
- Cosine Similarity is better than Euclidean distance for sparse high-dimensional data
- Hybrid systems combine strengths of both — that's why Netflix uses them!
- Pearson Correlation handles rating bias better than raw similarity scores

---

## 👩‍💻 Author

**Maryam** — AI/ML Engineer  
🔗 [GitHub](https://github.com/saifmaryam) | 🤗 [HuggingFace](https://huggingface.co/spaces/maryam-cheema-ai)

*Completed as part of VeloxCode Agency Internship Program*
