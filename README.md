# Recommender-Systems
#### ML701 Course Project, MBZUAI, 2022

A recommender system works like any other machine learning model. It takes in data, and outputs predictions. This project deals with collaborative filtering-based recommender systems for movies, where movie recommendations are based entirely on user-item ratings alone. Movie features such as genres or user demographics are not taken into consideration in this approach. The problem space can be defined as a combination of a prediction engine and a recommendation engine: given a user u, predict the user's rating for a given movie m; and given a user watched a movie m, recommend the next movies that they might watch. Our contribution is a comparative study of three common approaches to building recommender systems, namely Nearest Neighbors, Matrix Factorization, and Multi-layer Perceptrons, with a focus on the accuracy of predicted movie ratings.

##Dataset
MovieLens 100K dataset - https://grouplens.org/datasets/movielens/100k/
Movie rating dataset collected by the GroupLens Research Project at the University of Minnesota. Stable benchmark dataset with 100,000 ratings from 943 unique users on 1682 unique movie IDs. Ratings are made on a 5-star scale, from 1-5. 
