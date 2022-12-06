# Machine Learning Algorithms for Recommender Systems
#### ML701 Course Project, MBZUAI, 2022

A recommender system works like any other machine learning model. It takes in data, and outputs predictions. This project deals with collaborative filtering-based recommender systems for movies, where movie recommendations are based entirely on user-item ratings alone. Movie features such as genres or user demographics are not taken into consideration in this approach.   
The problem space can be defined as a combination of a prediction engine and a recommendation engine: given a user u, predict the user's rating for a given movie m; and given a user watched a movie m, recommend the next movies that they might watch. Our contribution is a comparative study of three common approaches to building recommender systems, namely Nearest Neighbors, Matrix Factorization, and Multi-layer Perceptrons, with a focus on the accuracy of predicted movie ratings.

## Baseline Experiments

### Random Recommender
Recommends a sample of 10 random movies to any given user. Catalog coverage  is very high, but non-personalized.

### Popularity based Recommender
Recommends the most rated/popular movies to all users. Underrepresents less-known movies. 

### Item-Item Recommender
Recommends similar movies based on cosine/euclidean/manhattan distance between input movie and movies in the dataset. Applied normalization technique and studied results qualitatively.

## Methods Studied:
### Nearest Neighbour Collaborative Filtering Recommenders
The nearest neighbour collaborative filtering method is a memory-based technique. It has two approaches - a user-user approach and an item-item approach. The similarity between users or items is computed in a multidimensional space using a similarity metric. 
In the user-based approach, the recommender system mines the database to find correlations between users and identify how much different users agree on the movies they like. 
The item-based approach looks for similarities between movies, and recommends the most similar movies to the user's already-rated movies. 

### Matrix Factorization based Recommender
The idea is to find two matrices such that their product approximates the original rating matrix, ie, to find two matrices W of size m*k and H of size k*n such that the rating matrix R of size m*n is  R = WH. Initialize the two matrices with some random values and compute how different the product is from the original matrix. 
The difference is minimised iteratively using coordinate descent algorithm to find the local minimum. 

### MLP Based Recommender
Embeddings are used to co - evolve user and item latent features - make recommendations based on user interests. MLP layers map latent vectors to prediction scores.

## Dataset
MovieLens 100K dataset - https://grouplens.org/datasets/movielens/100k/  

Movie rating dataset collected by the GroupLens Research Project at the University of Minnesota. Stable benchmark dataset with 100,000 ratings from 943 unique users on 1682 unique movie IDs. Ratings are made on a 5-star scale, from 1-5. 
