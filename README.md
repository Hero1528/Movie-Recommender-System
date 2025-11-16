# Movie Recommender System

## 📌 Project Overview

Recommender Systems provide personalized suggestions for items that are most relevant to each user by predicting preferences according to user's past choices. They are used in various areas like movies, music, news, search queries, etc. These recommendations are made in two ways: 

1. Collaborative filtering: Collaborative filtering makes recommendations based on user's past behavior and similar decisions made by other users to predict items user may be interested in. For example, if User A likes movies X and Y and User B likes Y and Z then system might recommend movie Z to User A.
2. Content-based filtering: Content-based filtering recommends items based on the features of the items and the user's past preferences. For example, if a user likes action movies the system will recommend other action movies based on genres, actors or directors.


## 📊 Dataset Overview

In this project we are using 2 datasets namely "file.tsv" and "Movie_Id_Titles.csv". We combine both the datasets into a single csv file which contains the following column names as attributes: 

| Column Name           | Description |
|-----------------------|-------------|
| **user_id**           | Unique ID for every row |
| **item_id**           | Indicates the category to this movie belongs to |
| **rating**            | Indicates the rating that particular movie has got |
| **timestamp**         | Indicates the timestamp that rating |
| **title**             | It states the name of the movie |

---

## 🛠️ Techniques Used

### ✅ Content-Based Filtering
- Recommends similar movies based on content features (e.g., genre, cast, description).
- Uses techniques like:
  - TF-IDF (Term Frequency-Inverse Document Frequency)
  - Count Vectorization
  - Cosine Similarity

### ✅ Collaborative Filtering (if implemented)
- Suggests movies based on user ratings and behavior.
- Uses user-item interactions to find similar users or movies.

---

## ⚙️ Tools & Technologies

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Libraries Used:**
  - `pandas`, `numpy` for data processing
  - `scikit-learn` for vectorization and similarity computation
  - `nltk` for text preprocessing (if applicable)
  - `pickle` for model persistence
  - `streamlit` or `flask` (if web deployment is involved)

---

## 🔍 Key Steps

1. **Data Cleaning**
   - Removing nulls, duplicates
   - Parsing JSON-like columns

2. **Feature Engineering**
   - Creating a “tags” field combining relevant text features
   - Applying text vectorization (TF-IDF or Count Vectorizer)

3. **Similarity Computation**
   - Computing cosine similarity between movies

4. **Recommendation Function**
   - A function that takes a movie title and returns top N similar movies

5. **Optional UI/Deployment**
   - Creating a simple web interface using Streamlit or Flask to test the recommender

---

## 📈 Output

- A function (e.g., `recommend('Avatar')`) that returns similar movies
- Ranked list based on similarity scores
- Optional visualizations (e.g., popularity charts, genre distribution)

---
