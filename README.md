# Book-Recommender-System-project
Description This project implements a book recommendation system using two different approaches: a popularity-based recommender system and a collaborative filtering-based recommender system. The dataset used for this project includes information about books, users, and their ratings.

# Book Recommender System

This repository contains a Book Recommender System developed using Python, Pandas, and scikit-learn. The system includes both a popularity-based recommender and a collaborative filtering-based recommender.

## Project Overview

The project uses three datasets: `books`, `users`, and `ratings`. The primary goal is to recommend books to users based on their reading history and preferences.

### Datasets

- `books.csv`: Contains details about the books.
- `users.csv`: Contains details about the users.
- `ratings.csv`: Contains the ratings given by users to books.

### Main Features

1. **Popularity-Based Recommender System**:
   - Recommends books based on their popularity (number of ratings and average rating).
   - Filters books with at least 250 ratings and sorts them by average rating.

2. **Collaborative Filtering-Based Recommender System**:
   - Recommends books based on similarity to other books.
   - Uses user-book interaction matrix and cosine similarity for recommendations.

## Setup Instructions

### Prerequisites

- Python 3.x
- Pandas
- NumPy
- scikit-learn
- Jupyter Notebook (optional, for running the notebook interactively)

## Description
This project implements a book recommendation system using two different approaches: a popularity-based recommender system and a collaborative filtering-based recommender system. The dataset used for this project includes information about books, users, and their ratings.

## Project Overview
# Data Loading and Preprocessing:

Load the data from CSV files (books.csv, users.csv, and ratings.csv) using pandas.
Check for missing values and handle them accordingly.
Check for duplicate entries and remove them if necessary.
## Popularity-Based Recommender System:

Merge the ratings and books data to include book titles in the ratings dataframe.
Calculate the number of ratings and the average rating for each book.
Create a dataframe of popular books by filtering books with a minimum number of ratings and sorting by average rating.
Select the top 50 books to recommend.
### Collaborative Filtering-Based Recommender System:

Filter users who have rated more than 200 books to focus on more reliable data.
Filter books that have been rated by at least 50 users.
Create a pivot table where rows represent books and columns represent users, with ratings as values.
Fill missing values in the pivot table with zeros.
Calculate the cosine similarity between books based on user ratings.
Implement a recommendation function to fetch books similar to a given book based on cosine similarity scores.
# Saving the Model:

Use pickle to save the popularity-based recommendations, pivot table, book data, and similarity scores for future use.
How to Use
## Popularity-Based Recommendations:

Run the script to get the top 50 popular books based on the number of ratings and average rating.
## Collaborative Filtering-Based Recommendations:

Use the recommend function to get book recommendations similar to a given book.
Pass the book title to the function to get a list of similar books along with their authors and cover images.

