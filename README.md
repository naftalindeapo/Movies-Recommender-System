# Movies-Recommender-System
In recent years, the explosion of data and the popularity of e-commerce and streaming platforms have made personalized recommendations a vital component of many businesses. From Amazon to Netflix, recommendation engines have become ubiquitous in modern online commerce. This repository provides access to the notebook used to obtain the results for a [technical report](https://drive.google.com/uc?id=1fcvNiU6CGfjQSWAayQ-77xRBOr1Gk3GY) showcasing a prototype of a recommendation engine we have developed and explaining its value to any business: a case study of Applied Machine Learning at Scale. 

Our recommendation engine is based on collaborative filtering, a technique that analyzes the preferences and behaviours of users to recommend items they might like. This is a popular technique for building recommendation systems, which relies on the idea that users with similar preferences will have similar preferences in the future. This method can be used for various item recommendations, such as books, music, and movies, and is effective in many real-world applications. Our prototype will use the Alternating Least Squares (ALS) algorithm, a matrix factorization method that can handle large datasets and effectively capture user-item interactions. Our engine also incorporates content-based filtering by considering movie genres to improve the accuracy of recommendations.

# Datasets
In this practical, we used the [MovieLens 100K](https://grouplens.org/datasets/movielens/100k/) and [MovieLens 25M](https://grouplens.org/datasets/movielens/25m/) datasets, which comprise user ratings and movie metadata. The Movielens 100K rating dataset consists of 100836 movie ratings given by 610 users for 9742 movies, while the MovieLens 25M rating dataset consists of over 25 million movie ratings provided by 162541 users for approximately 59047 movies.

## Rating Distribution
The ratings range from 0.5 to 5 stars, and the distribution of ratings appears to follow a power law, with the majority of ratings falling in the 3-4 star range as shown in Figure 1 below.
![alt text](https://drive.google.com/uc?id=1Q53v607-j_uBQkz4G7OY6CPY7x2xpzzK) 

## Power Laws Distribution
The MovieLens dataset provides a rich source for building and evaluating recommendation systems. We also plotted the power laws distribution for the two MovieLens datasets, as shown in Figure 3.
![alt text](https://drive.google.com/uc?id=1Ls3bAMxwN1zQItkGagkxuyuGDCnQ5hdG) 

The power law distributions suggest that a few movies and users account for a large portion of the ratings, which can be essential to consider when designing and evaluating recommendation algorithms.

## The Distribution of Movie Genres.
The movie metadata includes the movieId, title, release year, and genre. There are 20 unique genres in the dataset, the most common being Drama, Comedy, and Thriller. Some movies have multiple genres, and the distribution of genres follows a power law, with Drama being the most common genre. Figure 4 below shows the distribution of movie features/genres.
![alt text](https://drive.google.com/uc?id=1SuoPBUAvI-6eURi57CPq54rdVShNpkpi) 

# MLE for user and item biases, and latent trait vectors using ALS
ALS algorithm with user and item biases and latent trait vectors incorporate user and item biases with user and item latent factors by adding additional variables that represent the underlying characteristics of users and items, which can be learned through the ALS algorithm using a similar approach to that used for biases. The performance of the model is evaluated using the root mean squared error (RMSE) metric as shown in Figure 6 below.
![alt text](https://drive.google.com/uc?id=1k9slkkb4M5PhKubX_bJT1MtrI6EYHoSb)  

# Experimental Results
### Embendings
After training the ALS algorithm, plotting the embeddings in a 2D space can give us insights into how users and items are related to each other based on their latent factors as shown in Figures 7 and 8 below. The embeddings allow us to visualize how movies with the similar features are embedded together and how opposite movies are embedded in ’opposite’ parts of the space. 
<div>
    <img src="https://drive.google.com/uc?id=1a2G6XT2MUzE9-uCNUEkHaEFtBUDP9W_W" style="width: 50%; float: left;" /> 
    <img src="https://drive.google.com/uc?id=1mEpGTDEZ2ZIBnhTopu72ug0IlGIVkuhK" style="width: 42%; float: right;" />  
 </div>

### Recommendations
To show that our recommendations make sense, we will create a “dummy user” who gave some movie like the “Lord of the Rings” five stars and see what are the top 10 recommendations. Below are the top 10 recommendations for the user who rated the “Lord of the Rings: The Fellowship of the Ring, The (2001)” 5 star rating.
![alt text](https://drive.google.com/uc?id=1REIVLN-lJg1bYXhgF-r6rlGx31CU1_pd)  

### The "Napolean Dynamite" Effect
The “Napoleon Dynamite effect” is a phenomenon where certain movies receive extremely high or extremely low ratings despite their overall quality. To demonstrate this effect after training an ALS model, we will calculate the average rating for each movie and plot the distribution of ratings as shown in Figure 12 below:
<div>
    <img src="https://drive.google.com/uc?id=1LKwInBydXI6V9-uBRAcv09tmnQDaG3gC" style="width: 36%; float: left;" /> 
    <img src="https://drive.google.com/uc?id=1iJaPD5OyUrMy6XtYVJXDrBB4ceekTCyu" style="width: 27%; float: right;" /> 
    <img src="https://drive.google.com/uc?id=1BLR5cU0d6_s75BGb7_gvH3WInRLnJi11" style="width: 34%; float: left;" /> 
 </div>


# Running the code

### Dependencies
- Anaconda 3
- Python 3
- Any CPU/GPU-supported device with at least 4 CPU cores

### License
Refer to the [LICENSE](https://github.com/naftalindeapo/Movies-Recommender-System/blob/main/LICENSE).
