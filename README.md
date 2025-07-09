# 🎬 Movie Recommendation System

A content-based recommender system that suggests similar Hollywood movies using **cosine similarity** on user ratings.

---

## 📁 Project Structure

- 📄 [hollywood_movie_ratings_200.csv](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/hollywood_movie_ratings_200.csv) — Dataset of 200 Hollywood movies and user ratings  
- 📔 [Movie_Recommendation_System.ipynb](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/Movie_Recommendation_System.ipynb) — Full Google Colab Notebook  
- 🎥 [Demo Video](https://drive.google.com/file/d/1VkVigo2hA8JFYQgOewPnM97EtE0tM63f/view?usp=sharing)

---

## 🎯 Objective

To build a recommender system using collaborative filtering (item-based) to personalize movie suggestions based on user preferences.

---

## ⚙️ Features

- ✅ Cosine similarity for finding similar movies
- ✅ User-movie ratings matrix
- ✅ Personalized top 5 movie recommendations
- ✅ Google Colab compatible
- ✅ Custom input for real-time movie suggestion

---

## 🚀 How to Use

1. Open the Colab Notebook from the link above.
2. Upload the CSV file when prompted.
3. Call the function like this:

```python
recommend_movies("A Quiet Place Part II")
📽️ Demo Video
🎬 Watch Demo on Google Drive

👩‍💻 Author
Khushi Sharma
GitHub: @khushisharma-hub

✅ Conclusion
This project showcases how content-based filtering can be used to create a movie recommendation system using simple Python tools. It’s ideal for beginners in machine learning and data science.

🔗 Important Links
🔹 Dataset (CSV)

🔹 Google Colab Notebook

python
Copy
Edit

---

## 🧠 Full Google Colab Code

```python
# ✅ STEP 1: Upload the CSV File
from google.colab import files
import pandas as pd
import io

uploaded = files.upload()  # Upload hollywood_movie_ratings_200.csv
filename = next(iter(uploaded))
df = pd.read_csv(io.BytesIO(uploaded[filename]))

print("📥 Dataset Loaded Successfully!")
print(df.head())

# ✅ STEP 2: Create User-Movie Ratings Matrix
user_movie_matrix = df.pivot_table(index='UserID', columns='Movie', values='Rating')
print("\n🎥 User-Movie Ratings Matrix Preview:")
print(user_movie_matrix.head())

# ✅ STEP 3: Fill NaN with 0 for cosine similarity calculation
movie_matrix_filled = user_movie_matrix.fillna(0)

# ✅ STEP 4: Compute Cosine Similarity Between Movies
from sklearn.metrics.pairwise import cosine_similarity

cosine_sim = cosine_similarity(movie_matrix_filled.T)  # transpose: items instead of users
similarity_df = pd.DataFrame(cosine_sim, 
                             index=movie_matrix_filled.columns, 
                             columns=movie_matrix_filled.columns)

# ✅ STEP 5: Movie Recommender Function
def recommend_movies(movie_name, similarity_matrix=similarity_df, top_n=5):
    if movie_name not in similarity_matrix.columns:
        print(f"❌ Movie '{movie_name}' not found in the dataset.")
        print("🔎 Tip: Use print(df['Movie'].unique()) to list available movie names.")
        return
    print(f"\n🎬 Because you watched **{movie_name}**, you might also like:")
    recommended = similarity_matrix[movie_name].sort_values(ascending=False)[1:top_n+1]
    for movie, score in recommended.items():
        print(f"👉 {movie} (Similarity Score: {score:.2f})")

# ✅ STEP 6: Try with a Sample Movie
print("\n🔍 Available Movies:\n", df['Movie'].unique()[:10])  # Show some available movies
recommend_movies("A Quiet Place Part II")
