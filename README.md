# 🎬 Movie Recommendation System

A content-based movie recommender system that suggests similar Hollywood movies using **cosine similarity** on user ratings.

---

## 📁 Project Structure

- [hollywood_movie_ratings_200.csv](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/hollywood_movie_ratings_200.csv) — Dataset of 200 Hollywood movies and user ratings
- [Movie_Recommendation_System.ipynb](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/Movie_Recommendation_System.ipynb) — Full Google Colab code notebook

---

## 🎯 Objective

To build a recommender system using collaborative filtering (item-based) to personalize movie suggestions based on user ratings.

---

## ⚙️ Features

- ✅ Content-based filtering using cosine similarity
- ✅ Pandas pivot table for user-movie matrix
- ✅ Recommender function that suggests top 5 similar movies
- ✅ Google Colab compatible
- ✅ User input option for testing recommendations

---

## 🚀 How to Run

1. Open the `.ipynb` file in Google Colab or Jupyter.
2. Upload the CSV file when prompted.
3. Use the function:

```python
recommend_movies("A Quiet Place Part II")
 Sample Output
less
Copy
Edit
🎬 Because you watched A Quiet Place Part II, you might also like:
👉 A Quiet Place (Similarity Score: 0.89)
👉 It Chapter Two (Similarity Score: 0.86)
👉 Annabelle Comes Home (Similarity Score: 0.84)
👉 The Conjuring (Similarity Score: 0.83)
👉 The Nun (Similarity Score: 0.80)
📽️ Demo Video (Optional)
If you have a demo video, include it here:

Watch Demo

👩‍💻 Author
Khushi Sharma — GitHub Profile

🔗 Links
🔹 Dataset CSV File

🔹 Notebook (.ipynb)

✅ Conclusion
This project demonstrates how simple collaborative filtering and cosine similarity can be used to build a basic yet powerful movie recommendation system. It can be extended further into user-based systems or integrated into a web app using Streamlit.
