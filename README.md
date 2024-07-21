# Movie Recommendation Systems

Recommendation Systems are software tools and techniques that provide suggestions for items that are most likely of interest to a particular user. In this repository, we focus on Movie Recommendation Systems using two different approaches: SVD (Singular Value Decomposition) and Neural Networks with genre-based ratings.

## Recommendation System Taxonomy

There are two main types of recommendation systems:

1. **Non-Personalized**
    - Most-Popular
    - Highest Rated

2. **Personalized**
    - Content-Based
    - Collaborative
        - Nearest-Neighbor
        - Latent Factorization (Matrix Factorization)
    - Context-Aware
        - Factorization Machine
        - Deep Learning
    - Hybrid

## Input Data

The input data for recommendation systems is typically a Rating Matrix, where users are arranged in rows, items (movies) in columns, and each entry represents the rating of a user for a particular item. The rating matrix is mostly sparse, with density often less than 0.01%.

## Single Value Decomposition (SVD)

SVD decomposes a matrix of any shape into a product of three matrices with nice mathematical properties: 

\[ A = USV^T \]

- \( A \): \( n x m \) (number of records as rows and number of dimensions/features as columns)
- \( U \): \( n x n \) (orthogonal matrix containing eigenvectors of \( A x A^T \))
- \( S \): \( n x m \) (ordered singular values in the diagonal, square root of eigenvalues associated with \( A x A^T \) or \( A^T x A \))
- \( V \): \( m x m \) (orthogonal matrix containing eigenvectors of \( A^T x A \))

## Neural Network Model with Genre-Based Ratings

In recommendation systems, user IDs are often used to represent which users have rated or interacted with which items (movies, products, etc.). By converting these user IDs to indices, we:

- Simplify the input data for neural networks or other models.
- Ensure compatibility and consistency when handling user-related data across different parts of the system (e.g., training, inference, evaluation).

### User ID to Index Mapping

The mapping of `user_id_to_index` facilitates the efficient handling and processing of categorical user IDs in machine learning applications. It ensures the data is suitable for numerical computations and maintains consistency across datasets and operations. This is primarily for efficient representation and processing within machine learning models, especially neural networks.

### Deep Learning Model

We employ a deep learning model to improve the recommendation system's accuracy by considering user interactions and item attributes, such as genres. This approach helps in providing more personalized recommendations by leveraging complex patterns in the data.

---

This repository contains two notebooks demonstrating the implementation of these approaches:

1. **Movie Recommendation System using SVD**
2. **Movie Recommendation System with Rating using Neural Network with Genre**

Feel free to explore the notebooks for detailed implementations and results.
