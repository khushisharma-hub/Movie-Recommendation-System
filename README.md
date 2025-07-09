# 🎬 Movie Recommendation System

A personalized content-based movie recommender system designed to suggest similar Hollywood movies based on user preferences using collaborative filtering.

---

## 📌 Internship Details

- **Internship Program**: Tamizhan Skills Rise Internship
- **Domain**: Machine Learning & AI
- **Intern ID**: TS-RISE-MLAI-2514
- **Project Title**: Movie Recommendation System
- **Author**: Khushi Sharma
- **GitHub Repository**: [Movie Recommendation System](https://github.com/khushisharma-hub/Movie-Recommendation-System)
- **Demo Video**: [Watch Demo](https://drive.google.com/file/d/1VkVigo2hA8JFYQgOewPnM97EtE0tM63f/view?usp=sharing)

---

## 📚 Table of Contents

1. [Project Overview](#project-overview)
2. [Objective](#objective)
3. [Dataset Description](#dataset-description)
4. [Technologies Used](#technologies-used)
5. [Project Workflow](#project-workflow)
6. [Features](#features)
7. [How It Works](#how-it-works)
8. [Demo Output](#demo-output)
9. [Conclusion](#conclusion)
10. [Important Links](#important-links)

---

## 🧩 Project Overview

Movie streaming platforms like Netflix, Prime Video, and Hulu use recommendation systems to improve user experience and engagement. This project demonstrates a simplified version of such a system using a dataset of 200 Hollywood movies and their user ratings. The system provides movie recommendations based on user preferences through collaborative filtering.

---

## 🎯 Objective

The objective of this project is to:

- Build a recommendation system that suggests similar movies to a given input.
- Use collaborative filtering and cosine similarity to identify related titles.
- Provide personalized recommendations based on historical ratings data.

---

## 🗃️ Dataset Description

- **File**: [hollywood_movie_ratings_200.csv](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/hollywood_movie_ratings_200.csv)
- **Format**: CSV
- **Total Movies**: 200
- **Columns**:
  - `UserID`: Unique user identifier
  - `Movie`: Movie name
  - `Rating`: User's rating of the movie (1-5 scale)

This dataset simulates a real-world ratings matrix where multiple users have rated various movies.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** for data processing
- **Scikit-learn** for similarity calculation
- **Google Colab** for development and testing
- **Cosine Similarity** for finding related movies
- **Collaborative Filtering** (item-based)

---

## 🔄 Project Workflow

1. **Data Upload**: Load the dataset into a Pandas DataFrame.
2. **Pivot Table**: Convert the data into a User-Movie matrix.
3. **Preprocessing**: Fill missing values with zeros to prepare for similarity calculation.
4. **Cosine Similarity**: Calculate the similarity between movies.
5. **Recommendation Function**: Retrieve top 5 similar movies for any given input.
6. **User Interaction**: User can input a movie name to get recommendations.

---

## ⭐ Features

- 🎞️ Suggests top 5 similar movies based on your input
- 💡 Easy-to-use and Google Colab compatible
- 📊 Uses real rating patterns to determine movie similarity
- 🔍 Displays list of available movie titles
- 📈 Efficient even with limited data (200 movies)

---

## 💡 How It Works

The recommender system works by calculating cosine similarity scores between movies based on how users rated them. If two movies are frequently rated similarly by many users, they will have a high similarity score. When a user inputs a movie name, the system sorts the similarity scores and returns the most closely related movies as suggestions.

---

## 📽️ Demo Output

After uploading the dataset and running the recommendation function with an input like:

**"A Quiet Place Part II"**

The system might return:

🎬 Because you watched A Quiet Place Part II, you might also like:
👉 A Quiet Place
👉 It Chapter Two
👉 Annabelle Comes Home
👉 The Conjuring
👉 The Nun

---

## ✅ Conclusion

This project is a great example of how **machine learning and data science** can be applied to personalize user experiences. Using a basic dataset and content-based filtering, we built a working recommendation engine that mimics the core logic used in streaming platforms.

It not only strengthens machine learning skills but also demonstrates real-world applicability of algorithms like cosine similarity and collaborative filtering.

---

## 🔗 Important Links

- 📂 Dataset CSV: [hollywood_movie_ratings_200.csv](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/hollywood_movie_ratings_200.csv)
- 📔 Colab Notebook: [Movie_Recommendation_System.ipynb](https://github.com/khushisharma-hub/Movie-Recommendation-System/blob/main/Movie_Recommendation_System.ipynb)
- 🎥 Demo Video: [Watch Here](https://drive.google.com/file/d/1VkVigo2hA8JFYQgOewPnM97EtE0tM63f/view?usp=sharing)

---
