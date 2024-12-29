# Book Recommendation System

This report details the development and evaluation of a book recommendation system.  The system utilizes collaborative filtering, content-based filtering, a hybrid approach, and a knowledge-based approach to provide diverse recommendations.  The system is built upon three datasets: Books.csv, Ratings.csv, and Users.csv.  Due to memory constraints with the original data size, the datasets were preprocessed to reduce the dataset size, drop columns, filter users and books to work effectively with the available system resources.


**1. Data Preprocessing:**

*   The (Year-Of-Publication) column was removed due to inconsistent data types.
*   A 10% random sample of books was taken, and the ratings data was filtered to include only interactions with the selected books.
*   The top 5000 most active users were chosen for the collaborative filtering model to reduce memory consumption and model training time.
*   A combined features column consisting of book title and author was created for content-based filtering.

**2. Recommendation Algorithms:**

*   **Collaborative Filtering:** A k-Nearest Neighbors (KNN) model with cosine similarity was used to identify users with similar rating patterns and recommend books they liked.
*   **Content-Based Filtering:**  TF-IDF vectorization was applied to book titles and authors to generate a book feature matrix. Cosine similarity was then used to find books with similar features.
*   **Hybrid Approach:**  Combines collaborative and content-based recommendations to leverage the strengths of both methods.
*   **Knowledge-Based Filtering:**  Allows users to filter books based on author or publisher.

**3. System Output and Evaluation:**

The system generates recommendations using each of the implemented methods. Recommendations are displayed as tables including book details and scores.  Example recommendations are provided for a random book and an active user from the data.

**4. Visualizations:**

Several visualizations provide insights into the data:

*   **Book Ratings Distribution:** A histogram shows the frequency of different book ratings, indicating the popularity distribution of books in the dataset.

*   **Top 10 Authors and Publishers:** Bar plots illustrate the authors and publishers with the highest number of books in the dataset, showcasing dominance within the book collection.

*   **Average Rating per Book:** Distribution of average book ratings across the dataset provides insight into the overall quality perception of the books present in the database.


**5. Challenges and Future Work:**

* **Scalability:** The system currently uses a reduced dataset for memory efficiency. Improvements are needed to handle the full dataset or use distributed computing approaches.

* **Cold Start Problem:** The collaborative filtering approach has issues with new users and items.  Hybrid methods might improve the model’s performance but additional techniques such as incorporating metadata or using implicit feedback data can be considered.

* **Performance Metrics:** More comprehensive evaluation metrics (precision, recall, NDCG) should be used to evaluate the performance of each algorithm.


**6. Conclusion:**

The developed book recommendation system effectively leverages different filtering methods. The visualizations offer valuable insights into the book dataset.  Future enhancements will focus on scalability, addressing cold-start issues, and more rigorous evaluations to create a more robust recommendation system.
