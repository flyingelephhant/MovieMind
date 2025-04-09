# 🎥 MovieMind - Intelligent Movie Rating & Recommendation System

Welcome to the **MovieMind** project!  
In this project, we use machine learning techniques to predict IMDb ratings for both new and existing movies and provide personalized movie recommendations based on genre similarity.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Project Details](#project-details)
  - [Data Collection](#data-collection)
  - [Data Preprocessing](#data-preprocessing)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Feature Engineering](#feature-engineering)
  - [Modeling](#modeling)
  - [Evaluation](#evaluation)
  - [Recommendation System](#recommendation-system)
- [Conclusion](#conclusion)
- [References](#references)

---

## 📖 Project Overview

The goal of this project is to build an end-to-end movie rating prediction system that can:
- Predict IMDb ratings based on director, actors, genres, and duration.
- Handle cold start problems (new directors/actors) using TMDb API.
- Provide fuzzy matching for better user input handling.
- Recommend similar movies based on selected genres.

The system helps users get an estimated rating and recommendations even if proper historical data for the movie is not available.

---

## 🚀 Getting Started

### Prerequisites

To run this project, make sure you have:

- Python 3.x
- Jupyter Notebook (optional, if you want to run `.ipynb`)

You will also need the following Python libraries:

- pandas
- numpy
- matplotlib
- seaborn
- requests
- thefuzz
- scikit-learn
- xgboost
- pickle-mixin

### Installation

To install all required libraries, open your terminal and run:

```bash
pip install -r requirements.txt
```

🖥️ Usage
-Open the Jupyter notebook file Movie_Rating.ipynb or run the Python script.

# Provide the following user inputs when prompted:
  🎬 Director's name
  🎭 Actor 1 name
  🎭 Actor 2 name
  🎞️ Genres (comma-separated)
  ⏱️ Movie duration in minutes

The system will:
  ⭐ Predict the IMDb rating
  ✅ Provide a recommendation category
  🎯 Suggest similar movies based on genre

# 🔍 Project Details
  Data Collection
  We use a cleaned dataset Movie_Dataset_p.csv, which contains:
    🎥 Movie titles
    🎬 Director names
    🎭 Actor names
    🎞️ Genres
    ⭐ IMDb ratings
    ⏱️ Runtime
    🗣️ Language  
For missing or unknown directors/actors, the system fetches data from TMDb API to improve accuracy.

# Data Preprocessing
  Preprocessing steps include:
    Handling missing values
    Cleaning whitespace and special characters
    Standardizing text cases (lowercasing names)
    Filling missing runtime and language values
    Cleaning genres and actors/director name
    Exploratory Data Analysis (EDA)
    Visualized IMDb score distributions
    Analyzed impact of duration on IMDb scores
    Analyzed correlation between director's average rating and IMDb score
    Created visual plots using Matplotlib and Seaborn

# Feature Engineering
  Calculated average ratings for directors and actors
  One-hot encoded movie genres using MultiLabelBinarizer
  Built feature vectors for model training

# Modeling

  We trained multiple regression models:
    Linear Regression
    Random Forest Regressor
    XGBoost Regressor
    K-Nearest Neighbors
    Multi-layer Perceptron (MLP)

✅ The final selected model is Random Forest Regressor for its high accuracy.
 
Models and preprocessing data are saved using Pickle for easy deployment.

# Evaluation
    We evaluated model performance using:
    📉 Mean Squared Error (MSE)
    📈 R² Score

The Random Forest model performed the best in predicting IMDb ratings.

# Recommendation System
    Based on genre similarity, we use cosine similarity to recommend similar movies.
    The system outputs the top 5 recommended movies along with their genres and IMDb scores.

## ✅ Conclusion
In this project, we successfully built an end-to-end movie rating prediction and recommendation system.

## We implemented:

  ✅ Data cleaning and feature engineering

  🧩 Robust input handling with fuzzy matching

  🌟 Cold-start problem handling via TMDb API

  🔮 Machine learning models to predict ratings

  🎯 Genre-based movie recommendation engine

# 🔗 References
TMDb API
Pandas
Scikit-learn
Matplotlib
Seaborn
XGBoost
TheFuzz
