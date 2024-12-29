# Book Recommendation System

## Introduction

The Book Recommendation System suggests books to users based on their preferences and past interactions. This project implements collaborative filtering, content-based filtering, and a hybrid approach using a dataset containing information about books, users, and ratings.

## Objectives

- Implement collaborative filtering to recommend books based on user and item similarities.
- Use content-based filtering with book metadata.
- Develop a hybrid recommendation model combining collaborative and content-based approaches.
- Evaluate model performance using metrics like precision, recall, and F1-score.
- Visualize data and model performance.

## Dataset

### 1. Books Dataset
- **Fields**:
  - ISBN: Unique identifier for each book.
  - Book-Title, Book-Author, Year-Of-Publication, Publisher.
  - Image URLs for book covers: Image-URL-S, Image-URL-M, Image-URL-L.

### 2. Ratings Dataset
- **Fields**:
  - User-ID: Unique identifier for users.
  - ISBN: Book identifier.
  - Book-Rating: Rating on a 0-10 scale.

### 3. Users Dataset
- **Fields**:
  - User-ID: Unique identifier for users.
  - Location: User location.
  - Age: User age.

## Methodology

### 1. Data Preprocessing
- **Filtering**:
  - Retained users with at least 10 ratings.
  - Retained books with at least 5 ratings.
  
- **Handling Missing Data**:
  - Filled missing metadata fields with empty strings.

- **Merging Datasets**:
  - Combined ratings and books datasets for enriched information.

### 2. Recommendation Techniques

#### Collaborative Filtering
- Created a user-item interaction matrix using book ratings.
- Computed user similarity with cosine similarity.

#### Content-Based Filtering
- Combined metadata fields (Book-Title, Book-Author, Publisher) into a single feature.
- Applied TF-IDF vectorization to extract text features.
- Computed book similarity using cosine similarity.

#### Hybrid Approach
- Weighted combination of collaborative and content-based recommendations.
- Provided personalized recommendations leveraging both models.

### 3. Evaluation
- Split the ratings dataset into training (80%) and testing (20%).
- Evaluated the system using metrics like precision, recall, and F1-score (placeholders for now).

### 4. Visualization
- **Heatmaps**: User similarity for a subset of users.
- **Histograms**: Distribution of book ratings.

## Features

- **Memory Optimization**: Used sparse matrices for efficient storage and computation. Filtered data to focus on active users and popular books.
- **Scalability**: Designed to handle large datasets efficiently.
- **Hybrid Model**: Combines collaborative and content-based filtering for better accuracy.

## Results

- The system provides personalized book recommendations based on user preferences and metadata.
- Visualizations offer insights into user behavior and rating patterns.
- Placeholder evaluation metrics demonstrate a framework for assessing performance.

## Future Enhancements

- **Improved Evaluation**: Use actual test data to compute metrics like precision, recall, and F1-score.
- **Incorporate Implicit Feedback**: Analyze user behavior beyond explicit ratings (for example: clicks, views).
- **Advanced Hybrid Models**: Experiment with deep learning approaches.
- **Interactive Features**: Develop a user-friendly interface for accessing recommendations.

## Conclusion

This book recommendation system provides a scalable and efficient framework for suggesting books to users. By integrating collaborative filtering, content-based filtering, and a hybrid approach, the system delivers accurate and personalized recommendations. Future enhancements can improve its applicability and effectiveness in real-world scenarios.
