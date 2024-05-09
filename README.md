# Analysis-of-Customer-Data-Using-Recommender-Systems
# MovieLens Recommender System Analysis

## Project Description
This project involves the development and optimization of two types of recommender system models using the MovieLens dataset: one based on neighborhood methods and another on matrix factorization. Our objective is to enhance the quality of recommendations through meticulous hyperparameter tuning and comparative analysis against a baseline model.

## Dataset Overview
We utilize the MovieLens dataset, which comprises over 27 million ratings across 58,098 movies by 283,228 users. This rich dataset provides a foundation for exploring user preferences and improving recommendation accuracy.

## Exploratory Data Analysis (EDA)
The initial phase of our project involves an extensive EDA to understand underlying patterns within the data:
- **Stratified Sampling**: We employ StratifiedShuffleSplit to ensure each subgroup is represented, improving the reliability of our insights.
- **Comparative Analysis**: We analyze both the sampled and original datasets to confirm consistency across distributions.

## Models and Hyperparameter Tuning
### KNNWithZScore (Neighborhood-Based Method)
- **Parameters**:
  - `k`: Number of neighbors. Chosen to enhance personalized recommendations.
  - `min_k`: Minimum number of neighbors required for predictions, allowing inclusivity for new users.
  - `sim_options`: Pearson correlation for similarity, focusing on user rating patterns.
  - `user_based`: Both user-focused and movie-focused strategies are evaluated to optimize personalization.

### SVD++ (Matrix Factorization-Based Method)
- **Parameters**:
  - `n_factors`: Number of latent factors to capture complex patterns.
  - `n_epochs`: Number of iterations for training.
  - `lr_all`: Learning rate for updates.
  - `reg_all`: Regularization to prevent overfitting.
  - `biased`: Incorporation of bias terms to enhance model predictions.

## Results
Our analysis demonstrates that the SVD++ model performed the best in terms of RMSE, indicating its superior ability to handle both explicit and implicit feedback. Key findings include:

- The **SVD++ model** had a 5% lower RMSE compared to the KNNWithZScore model, suggesting better accuracy.
- Hyperparameter tuning showed that reducing the `n_factors` in SVD++ below 20 decreased performance.
- Neighborhood methods were particularly effective for users with a high number of ratings.

For a detailed visualization of the results, see the [results folder](link-to-results-folder).



## Installation
To set up the project, clone the repository and install the required libraries:
```bash
git clone https://github.com/yourusername/movielens-recommender-analysis.git
cd movielens-recommender-analysis
pip install -r requirements.txt
