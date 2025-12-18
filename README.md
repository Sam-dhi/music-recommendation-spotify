
# Music Recommendation System using Spotify Data

This project builds a **content-based music recommendation system**
using Spotify audio features from a Kaggle dataset.

The goal is to recommend songs that sound similar to a given song,
while still keeping diversity and novelty in the recommendations.

---

## Dataset

- Source: Kaggle Spotify Tracks Dataset
- Each row represents a track with audio features such as:
  - danceability
  - energy
  - valence
  - tempo
  - acousticness
  - instrumentalness
- Genre information (`track_genre`) is used only for analysis and interpretation.

---

## What I did in this project

### 1. Exploratory Data Analysis (EDA)
- Checked missing values and cleaned the dataset.
- Studied feature distributions and correlations.
- Used **Yellowbrick** to visualize correlations between audio features.

### 2. Feature Engineering
- Selected key audio features relevant to musical similarity.
- Standardized features using `StandardScaler`.

### 3. Clustering using K-Means
- Used the **Elbow Method** to choose the optimal number of clusters.
- Applied **K-Means clustering** to group songs with similar audio characteristics.
- Interpreted clusters based on average feature values.

### 4. Content-Based Recommendation
- Given a song name:
  - Identify its cluster.
  - Compute similarity using **Euclidean distance** in feature space.
  - Recommend the closest songs from the same cluster.
- This ensures recommendations are:
  - acoustically similar
  - novel (not exact duplicates)
  - genre-aligned in practice

---

## Example Output

For the input song:Blinding Lights

The model recommends tracks from different genres but with similar
audio characteristics such as tempo, energy, and valence.

This behavior is consistent with real-world music recommendation systems.

---

## Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Yellowbrick
- Matplotlib, Seaborn

---



