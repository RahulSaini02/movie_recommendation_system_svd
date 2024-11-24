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

## Installation and Running steps for Juypter Notebook

To set up the project locally, follow these steps:

1. Clone this repository:

   ```bash
   git clone git@github.com:RahulSaini02/movie_recommendation_svd.git
   ```

2. Navigate to the project directory:

    ```bash
    cd movies-recommendation-system
    ```
3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Download the above given dataset into the current directory

5. Open the .ipynb file in Juypter Notebook or Juypter Lab and run the cells
