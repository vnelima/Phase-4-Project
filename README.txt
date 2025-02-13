# Hybrid Movie Recommendation System

## Introduction
This project implements a **Hybrid Movie Recommendation System** that combines **Content-Based Filtering** and **Collaborative Filtering (SVD-based Matrix Factorization)**. The model is evaluated using standard recommendation metrics like **Precision@K, Recall@K, MAP@K, and NDCG@K**.

## Dataset
The dataset consists of user-movie interactions, including ratings and metadata like genres and tags. The data is preprocessed to create both a user-item matrix for collaborative filtering and a TF-IDF matrix for content-based filtering.

## Methodology
### 1. Content-Based Filtering
- TF-IDF vectorization is applied to genres and tags.
- k-Nearest Neighbors (k-NN) is used to find similar movies.
- Content-based scores are computed based on movies a user has rated highly.

### 2. Collaborative Filtering (SVD)
- A user-movie matrix is constructed.
- Truncated SVD reduces dimensionality.
- Cosine similarity is used to identify similar users and recommend movies.

### 3. Hybrid Model
- The collaborative filtering and content-based scores are combined using a weighted approach to generate final recommendations.

## Implementation
The system follows these key steps:
1. **Data Preprocessing** - Cleaning and transforming data for both filtering methods.
2. **Model Training** - Applying TF-IDF and SVD to create recommendation components.
3. **Hybrid Recommendation Generation** - Merging both models' outputs.
4. **Evaluation Metrics** - Assessing recommendation quality.

## Results
| Model Type                   | Precision@5 | Recall@5  | Precision@10 | Recall@10 |
|------------------------------|------------|-----------|--------------|------------|
| Content-Based Filtering      | 0.0        | 0.0       | -            | -          |
| Collaborative Filtering (SVD) | 0.8000     | 0.0205    | -            | -          |
| Hybrid Model (Initial)       | 0.8000     | 0.0205    | -            | -          |
| Improved Hybrid Model        | -          | -         | 0.9000       | 0.0462     |

**Visualization**
image 1.png
image 2.png
image 3.png
image 4.png
image 5.png
image 6.png
image 7.png

## Evaluation Metrics
1. **Precision@K** - Measures how many recommended movies are relevant.
2. **Recall@K** - Measures how many relevant movies are retrieved.
3. **MAP@K** - Evaluates the ranking quality of relevant items.
4. **NDCG@K** - Considers ranking and relevance to measure recommendation quality.

## Conclusion & Future Improvements
- The hybrid model improves precision and recall over collaborative filtering alone.
- Future enhancements can focus on tuning content weight and incorporating more contextual features.

## Usage
1. Load the dataset.
2. Run the notebook to preprocess data and train models.
3. Call the `hybrid_recommendations(user_id, num_recommendations=10)` function.
4. Evaluate results using the provided metrics.

## Dependencies
- Python 3.x
- Pandas, NumPy
- Scikit-learn
- Matplotlib/Seaborn (for visualizations)

## Author
Nelima

