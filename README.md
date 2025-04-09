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
