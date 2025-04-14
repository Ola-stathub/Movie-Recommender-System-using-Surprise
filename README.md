# Movie-Recommender-System-using-Surprise

🎬 Movie Recommendation System using Collaborative Filtering
📌 Project Overview
This notebook demonstrates how to build a Collaborative Filtering movie recommendation system using the scikit-surprise library. The project is structured in two main parts:

Exploring and modeling with a built-in dataset from surprise.

Importing and using a custom movie ratings dataset for deeper analysis and personalized recommendations.

📁 Part 1: Using Built-in Dataset from surprise
Dataset Used: The built-in MovieLens 100k dataset.

Goal: Train a collaborative filtering model to predict user ratings.

Steps:

Loaded the dataset using Dataset.load_builtin('ml-100k').

Applied train-test split using train_test_split().

Trained a Singular Value Decomposition (SVD) model.

Evaluated model performance using Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE).

🧠 The SVD model learns latent user and item factors that capture hidden preferences and item characteristics.

📁 Part 2: Custom Movie Ratings Dataset
Dataset: A custom DataFrame consisting of user ratings, movie titles, genres, and timestamps.

Columns Included: userId, movieId, rating, timestamp, title, genres.

🧪 Steps Performed:
Data Exploration:

Checked for missing values and data types.

Explored rating distributions and popular movies.

Data Formatting:

Converted the DataFrame into surprise’s required format (Dataset.load_from_df).

Prepared a Reader object with the appropriate rating scale.

Model Training:

Trained another SVD model using the custom dataset.

Predicted ratings for a given user.

Recommendations:

Generated top-N movie recommendations for individual users.

Filtered out movies the user has already rated.

Sorted predictions to recommend highest-rated unseen movies.

🧠 Techniques Used
Collaborative Filtering:
Predicts user preferences based on historical rating patterns across many users.

Matrix Factorization (SVD):
Reduces the high-dimensional user-item matrix into latent feature vectors for better predictions.

scikit-surprise library:
A powerful toolkit specifically built for recommender systems, making it easy to train, test, and evaluate models.

📊 Evaluation
RMSE and MAE used to assess prediction accuracy.

Top-N recommendation strategy used for generating personalized suggestions.

✅ Future Improvements
Implement item-based collaborative filtering.

Add content-based filtering using movie genres.

Build a hybrid recommender.

Create a web app for interactive recommendations.
