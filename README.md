# Movies Recommendation System

This project is part of the CS685 Group Project and aims to create a robust Movies Recommendation System that uses data science techniques to recommend films based on user preferences and trends.

## Project Overview

The Movies Recommendation System utilizes a dataset from TMDB, focusing on English-language movies that have already been released. The system includes three main recommendation techniques:

1. **Content-Based Filtering**:
   - Analyzes movie overviews, genres, and keywords.
   - Uses TF-IDF (Term Frequency-Inverse Document Frequency) vectorization to process textual features.
   - Reduces dimensionality with Truncated SVD to improve performance.
   - Employs cosine similarity to identify the top ten movies similar to a given title.

2. **Demographic Filtering**:
   - Ranks movies based on popularity and ratings.
   - Calculates a "weighted rating" similar to IMDb’s, which balances the number of votes and the average rating.

3. **Trending Movies**:
   - Identifies the top trending movies based on popularity.
   - Filters for movies released within the past year to show the most current popular movies.

## Features

- **Movie Search**: Allows users to search for specific movies and get recommendations based on their content similarity.
- **Top Rated Movies**: Provides a list of the highest-rated movies based on demographic filtering.
- **Trending Movies**: Displays currently popular movies released within the last year.

## Data Set

[TMDB Dataset](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies)

## Data Preprocessing

The dataset undergoes the following preprocessing steps:

- **Filtering**: Limits the dataset to English-language movies and movies that have been released.
- **Text Vectorization**: Uses TF-IDF on movie overviews, genres, and keywords to extract relevant features for similarity matching.
- **Dimensionality Reduction**: Applies Truncated SVD to reduce computational load and enhance model efficiency.

## Feature Engineering

**1. TF-IDF Vectorization:**
   - The content column was vectorized using TF-IDF (Term Frequency-Inverse Document Frequency), producing a term-weighted matrix that highlights unique words in movie overview.

**2. Dimensionality Reduction:**
   - Truncated SVD reduced the high-dimensional TF-IDF matrix into 100 latent features.
        - Parameters:
           - n_components=70
           - random_state=42
**3. Normalization:**
   - Normalized the reduced matrix to ensure all vectors had equal magnitude, enabling fair cosine similarity comparisons.

## Similarity Computation

**1. Cosine Similarity:**
   - Used to Measure the similarity between feature vectors in the reduced space. The resulting similarity matrix serves as the base for retrieving movie recommendations.

**2. Recommendation Retrieval:**
   - Designed a function to retrieve the top 10 most similar movies for a given title based on the similarity matrix.

## Installation and Running steps for Jupyter Notebook

To set up the project locally, follow these steps:

1. Clone this repository:

   ```bash
   git clone git@github.com:RahulSaini02/movie_recommendation_system_svd.git
   ```

2. Navigate to the project directory:

    ```bash
    cd movie_recommendation_system_svd/jupyter_notebook
    ```
3. Set up Python virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # Activate the virtual environment
   ```
4. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

5. Download the above given dataset into the current directory

6. Running Jupyter Notebook

   ```bash
   jupyter notebook
   ```

## Results

![image](https://github.com/user-attachments/assets/b89d40eb-031e-43e9-8193-fe96dc6b25cc)

![image](https://github.com/user-attachments/assets/c86044f1-cf66-4317-8487-9e9539ef1f78)

![image](https://github.com/user-attachments/assets/024bef4a-5db0-4a75-8c8a-fbcf66fcf457)

![image](https://github.com/user-attachments/assets/e771124d-6ce7-4fc8-8867-3d8339ed8244)
