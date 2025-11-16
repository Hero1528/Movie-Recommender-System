🎬 Movie Recommender System
📌 Project Overview

Recommender Systems provide personalized suggestions by predicting what a user might like based on past behavior. They are widely used in platforms like movie apps, music streaming, e-commerce, and search engines.

There are two major types of recommendation approaches:

1. Collaborative Filtering

Makes recommendations using user behavior and similarities between users.

Example:
If User A likes movies X & Y, and User B likes Y & Z → Recommend Z to User A.

2. Content-Based Filtering (used in this project)

Recommends items based on their features (e.g., genre, actors, keywords).

Example:
If a user likes action movies → Recommend other action movies based on movie metadata.

📊 Dataset Overview

This project uses two datasets:

file.tsv

Movie_Id_Titles.csv

After merging, the final dataset contains:

Column Name	Description
user_id	Unique ID for each user
item_id	ID assigned to each movie
rating	Rating given by the user
timestamp	Timestamp of the rating
title	Movie title
🛠️ Techniques Used
✅ Content-Based Filtering

Recommends similar movies using:

TF-IDF

Count Vectorization

Cosine Similarity

Based on movie metadata and text processing.

✅ Collaborative Filtering (if implemented)

Suggests movies based on user-item interactions.

Uses rating patterns to find similar users or movies.

⚙️ Tools & Technologies

Language: Python

Environment: Jupyter Notebook

Libraries Used:

pandas, numpy — data processing

scikit-learn — vectorization & similarity computation

nltk — text cleaning (if used)

pickle — saving similarity matrix (optional)

streamlit / flask — for web interface (optional)

🔍 Key Steps
1. Data Cleaning

Remove null values

Handle duplicates

Merge datasets

2. Feature Engineering

Create a tags column combining key features

Apply CountVectorizer or TF-IDF

3. Similarity Computation

Compute cosine similarity between movies

Generate similarity matrix

4. Recommendation Function

A function like:

recommend("Avatar")


Returns top N most similar movies.

5. Optional UI

Create a simple interface using:

Streamlit

Flask

📈 Output

Input: recommend("Avatar")

Output: List of similar movies ranked by similarity score

Optional charts like:

Genre distribution

Movie popularity
