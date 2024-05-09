# Analysis-of-Customer-Data-Using-Recommender-Systems
# MovieLens Recommender System Analysis

## Project Description
This repository contains our project for analyzing customer data using the MovieLens dataset. The primary objective is to configure, evaluate, and compare different recommender system models. We focus on building and assessing a neighborhood-based method and a matrix factorization-based method against a baseline. This project aims to understand user preferences and improve recommendation accuracy.

## Dataset Information
The project uses the **MovieLens dataset** provided by GroupLens Research, which contains over 27 million five-star ratings across 58,098 movies and 283,228 users. All users have rated at least one movie. The dataset contains the following information:
- **UserID:** Unique identifier for each user
- **MovieID:** Unique identifier for each movie
- **Rating:** User-assigned rating for the movie (0.5 to 5.0 stars)
- **Timestamp:** When the rating was given, in UTC seconds since 1970

The dataset provides valuable insights into user preferences and is suitable for collaborative filtering techniques.

## Models Used
The project uses two different models:
1. **Neighborhood-Based Method:**
   - Implements the K-Nearest Neighbors (KNN) algorithm.
   - Uses similarities between user ratings to find similar neighbors and predict ratings.
   - Hyperparameters tuned include the similarity function (cosine similarity, Pearson correlation) and the minimum number of neighbors.

2. **Matrix Factorization-Based Method:**
   - Implements a matrix factorization algorithm, such as SVD.
   - Decomposes the user-item rating matrix into lower-dimensional matrices.
   - Hyperparameters tuned include the number of factors and learning rate.

**Baseline:**
- The baseline is a **normal predictor** that makes random predictions based on the distribution of the training set ratings.

## Installation
To run this project locally, follow these steps:
```bash
git clone https://github.com/yourusername/movielens-recommender-analysis.git
cd movielens-recommender-analysis
pip install -r requirements.txt
