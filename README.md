# Movie Recommendation System: Content-Based & Collaborative Filtering

## Overview

This project implements a recommendation system using two distinct approaches: Content-Based Filtering and User-Based Collaborative Filtering. The goal is to provide movie recommendations based on item attributes and user behavior, respectively, and compare both methods.

## Features

* **Content-Based Filtering:** Recommends items similar to those a user has liked in the past, based on item features.
    * Utilizes **Count Vectorizer** and **Cosine Similarity** to measure the likeness between item feature vectors.
* **User-Based Collaborative Filtering:** Recommends items that users with similar preferences have liked.
    * Employs the **k-Nearest Neighbors (k-NN)** algorithm to find users with similar tastes.
    * Uses **Cosine Similarity** to calculate similarity between user rating vectors.

## Algorithms Implemented

### 1. Content-Based Filtering

Content-Based Filtering works by analyzing the features of items a user has interacted with (e.g., liked, rated highly) and recommending other items with similar features.

* **Feature Representation:** Movie genres, cast and plot keywords were processed using Count Vectorization.
* **Similarity Metric:** Cosine Similarity was used to calculate the similarity score between the feature vectors of items.

### 2. User-Based Collaborative Filtering

User-Based Collaborative Filtering identifies users who have similar preferences to a target user and recommends items that these similar users have liked but the target user has not yet encountered.

* **User Similarity:** The k-Nearest Neighbors (k-NN) algorithm was used to identify the 'k' most similar users to a given user (in our code, we used 3 nearest neighbours).
* **Similarity Metric:** Cosine Similarity was applied to user-item rating vectors to determine the similarity between users.

## Dataset

* **Source:** TMDB 5000 Movie Dataset (https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata), "ratings.csv" in the repository
* **Description:** The former contains metadata of about 5000 movies with 24 columns split across 2 files, and the latter contains 408 ratings by 20 users.
* **Key Features Used:** Movie genres, cast of the movie, and keywords that describe the plot of the movie
