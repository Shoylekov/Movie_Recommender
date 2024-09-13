# Movie Recommender System
This project is a Movie Recommender System built using Streamlit for the web interface, and scikit-learn for feature extraction and similarity computation. The system allows users to select a movie from a dropdown menu and receive recommendations of similar movies along with their posters. The recommendations are based on text features such as movie descriptions (overview) and genres.

## Features
Movie Recommendations: The system recommends five movies similar to the one selected by the user.
Movie Posters: The application fetches and displays posters for the recommended movies using the TMDb API.
Cosine Similarity: It calculates similarity between movies based on textual data (movie overview and genres) using CountVectorizer and cosine_similarity.
Interactive Interface: The interface is built with Streamlit, allowing users to easily select a movie and view recommendations.

## Project Setup
Prerequisites
Python 3.x
### Libraries:
Streamlit
Scikit-learn
Pandas
Requests
Pickle

## How It Works
## Data Preparation:

The dataset contains information about movies including id, title, overview, and genre.
The overview and genre are combined into a tags column for each movie.
Using CountVectorizer, the tags are vectorized into numerical format, limiting to a maximum of 10,000 features.
The cosine similarity between the movie vectors is computed and stored in a similarity matrix.
This similarity matrix is used to find movies that are most similar to a selected movie.
## Recommendations:

When a user selects a movie from the dropdown menu, the app retrieves the index of the movie from the dataset.
Using the precomputed similarity matrix, the app finds the five most similar movies.
Movie titles and corresponding posters are fetched and displayed.
## API Integration:

The app fetches movie posters using the TMDb API by sending a request based on the movie's ID.
Posters are displayed alongside the recommended movie titles in the app.
![movie](https://github.com/user-attachments/assets/76ebb58d-c8ab-4dfa-94f5-9bc77973c4d9)
