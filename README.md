# Movie Recommendation System Content Based Filtering

## Overview
Movie Recommendation System

This is a content-based movie recommendation system built with Python. The system suggests movies that are similar to a given movie based on their description, genres, and keywords.

Features

Recommends top 5 similar movies for any movie in the dataset.

Uses movie overviews, genres, and keywords for similarity calculations.

Employs natural language processing (NLP) techniques to analyze text content.

Powered by Cosine Similarity for measuring how similar movies are.

How It Works

Load Dataset
We use the tmdb_5000_movies.csv dataset, which contains movie information such as title, overview, genres, and keywords.

Preprocess Data

Convert genres and keywords from JSON-like strings to lists.

Split movie overviews into individual words.

Combine overview, genres, and keywords into a single column called tags.

Convert all text to lowercase for uniformity.

Feature Extraction

Use CountVectorizer to convert text data into numerical vectors.

Consider a maximum of 5000 features and remove English stopwords.

Calculate Similarity

Compute Cosine Similarity between all movie vectors.

Cosine Similarity gives a score between 0 and 1 indicating how similar two movies are.

Make Recommendations

Given a movie title, the system finds the top 5 movies with the highest similarity.

Usage
# Example usage
recommend("Alien")
recommend("Harry Potter and the Half-Blood Prince")
recommend("Batman")


Sample Output:

Top 5 movies similar to 'Alien':

The Texas Chainsaw Massacre 2

Darkness

Eulogy

Dwegons

Hayride

Top 5 movies similar to 'Harry Potter and the Half-Blood Prince':

Harry Potter and the Goblet of Fire

Harry Potter and the Order of the Phoenix

Harry Potter and the Prisoner of Azkaban

Harry Potter and the Chamber of Secrets

Harry Potter and the Philosopher's Stone

Top 5 movies similar to 'Batman':

Batman & Robin

Batman Begins

The Dark Knight Rises

Batman Returns

The Dark Knight

Requirements

Python 3.x

pandas

numpy

scikit-learn

Install dependencies via pip:

pip install pandas numpy scikit-learn

Notes

The system is case-insensitive; you can type the movie title in any case.

Make sure the movie title exists in the dataset, otherwise it will throw an error.

Future Improvements

Integrate with a web interface for easy use.

Use TF-IDF or Word Embeddings for better recommendations.

Add poster images and links for a more interactive experience.

## Getting Started
Please refer to the source files for specific installation and usage instructions. Ensure that your local environment meets the standard requirements for the associated technologies.

## Project Structure
This project is organized into standard directories. Key configuration files and primary source code are located in the root directory.
