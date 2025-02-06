# recommender-system
# Movie Recommendation System

This Jupyter Notebook demonstrates a content-based movie recommendation system using machine learning. The system suggests movies similar to a user's favorite movie based on features like genres, keywords, tagline, cast, and director.

## Features
- **Content-Based Filtering**: Uses movie metadata to recommend similar movies.
- **TF-IDF Vectorization**: Converts text data into feature vectors.
- **Cosine Similarity**: Measures similarity between movies based on their features.

## Dataset
The dataset (`movies.csv`) contains information about **4803 movies** with features such as:
- `genres`
- `keywords`
- `tagline`
- `cast`
- `director`
- `title`
- And more.

## Workflow
1. **Import Libraries**: Uses `numpy`, `pandas`, `difflib`, and scikit-learn's `TfidfVectorizer` and `cosine_similarity`.
2. **Load Data**: Reads the CSV file into a DataFrame.
3. **Feature Selection**: Combines `genres`, `keywords`, `tagline`, `cast`, and `director` into a single text feature.
4. **Text Vectorization**: Converts combined text into TF-IDF feature vectors.
5. **Similarity Calculation**: Computes cosine similarity between all movies.
6. **User Input**: Takes a movie name from the user.
7. **Find Closest Match**: Uses `difflib` to handle typos/misspellings.
8. **Generate Recommendations**: Returns top 30 movies with the highest similarity scores.

## How to Use
1. **Prerequisites**:
   - Install required libraries:
     ```
     pip install numpy pandas scikit-learn
     ```
   - Download the dataset (`movies.csv`) and update the file path in the notebook.

2. **Run the Notebook**:
   - Execute all cells.
   - Enter a movie name when prompted (e.g., "iron man").
   - The system will display a list of recommended movies.

