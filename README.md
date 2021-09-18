# Movie-Recommendation-With-Recommenderlab

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

DataSet : https://grouplens.org/datasets/movielens/latest/

In this blog post, I will first explain how collaborative filtering works. Secondly, I’m going to show you how to develop your own small movie recommender with the R package recommenderlab and provide it in a shiny application.

Different Approaches
========================

There are several approaches to give a recommendation. In the user-based collaborative filtering (UBCF), the users are in the focus of the recommendation system. For a new proposal, the similarities between new and existing users are first calculated. Afterward, either the n most similar users or all users with a similarity above a specified threshold are consulted. The average ratings of the products are formed via these users and, if necessary, weighed according to their similarity. Then, the x highest rated products are displayed to the new user as a suggestion.

For the item-based collaborative filtering IBCF, however, the focus is on the products. For every two products, the similarity between them is calculated in terms of their ratings. For each product, the k most similar products are identified, and for each user, the products that best match their previous purchases are suggested.

Those and other collaborative filtering methods are implemented in the recommenderlab package:

    ALS_realRatingMatrix: Recommender for explicit ratings based on latent factors, calculated by alternating least squares algorithm.
    ALS_implicit_realRatingMatrix: Recommender for implicit data based on latent factors, calculated by alternating least squares algorithm.
    IBCF_realRatingMatrix: Recommender based on item-based collaborative filtering.
    LIBMF_realRatingMatrix: Matrix factorization with LIBMF via package recosystem.
    POPULAR_realRatingMatrix: Recommender based on item popularity.
    RANDOM_realRatingMatrix: Produce random recommendations (real ratings).
    RERECOMMEND_realRatingMatrix: Re-recommends highly-rated items (real ratings).
    SVD_realRatingMatrix: Recommender based on SVD approximation with column-mean imputation.
    SVDF_realRatingMatrix: Recommender based on Funk SVD with gradient descend.
    UBCF_realRatingMatrix: Recommender based on user-based collaborative filtering.
