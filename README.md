# Data-Mining-II
Projects developed under the Data Mining II college chair during the 2019/2020 school year

## Movie Recommendtion System

The Recommendation Problem is typically characterized by 2 objects: a set of users and set of items to be recommended to the users, and the goal is learning the function that maps the relevance and usefulness of a particular item for a user. There are two main prediction tasks that can be done depending on the context and data in our problem:
<ul>
  <li> Item Prediction: Gives an ordered list of items which are likely to be consumed or liked by the user on the future; </li>
  <li> Rating prediction: Gives a predicted rating that the user is likely to give to a certain item that he hasn't seen yet. </li>
</ul>

In the proposed assignment we are dealing with data collected from the website Flixter which is a social movie platform where the users can look for movie recommendations and also share their opinions and give ratings to movies they have seen. Given this we have the standard recommendation problem setting where our task is to predict the best movie recommendations to give to a user or the rating that a user might give to a movie.
  
In order to achieve this goal we start by performing an Exploratory Data Analysis where we first get to know the Datasets and informations available and then delve into the main features and behaviors captured by this data. Here we also do some Data Visualization that helped us understand which attributes are important to include in our models, which time periods are statistically significant, among others.
  
The following step was to build our recommendation algorithms. In the section Recommendation Models we begin by briefly explaining and giving examples of the reasoning behind each model's approach, followed by the experimental steps and implementation. The algorithms we have decided to work are based on the following approaches:
<ul> 
  <li> Popularity </li>
  <li> Association Rules </li>
  <li> Collaborative filtering </li>
  <li> Hybrid Approaches </li>
</ul>

And lastly we use several evaluation metrics to perform tests and comparisons between the performances of the models' implementations which we explain and show the results in a intuitive and visual way. To do this we train our models to learn the best recommendations in a given time period and then test those recommendations based on what the users have watched in reality in the following time period. For each model we calculate the Precision, Recall, F1-score and the percentage of users that have watched at least one of our recommendations, and those measures are given by the following:

![image](https://user-images.githubusercontent.com/13381706/163249894-9bf7f745-988e-4570-9dbe-7ee43c502593.png)

It is important to note that the number of movies that the user has watched in the same period is not the total number of movies the user has watched, but the number of movies he has watched within the subset of possible recommendations which we considered to be the 50 most popular movies of that time period.

For each type of approach we test the models for different numbers of recommendations that are given to the user, and then try to choose the best number based on the performance measures above. Here it is important to understand that according to the way the recall is calculated, the more recommendations we give, the higher will be the recall. Therefore there should be a compromise between this and the number of recommendations given, because it would not make sense to suggest too many movies to the user. After having the selected number of recommendation for each model we consecutively train and test all the models trough a sliding window to get the final results.

Due to github storage limitations, you can access the Flixer data here:

[ratings.csv](https://docs.google.com/spreadsheets/d/1ImLU_6lI79Ia4Bg5AfgWCs28tiSXpWqP/edit?usp=sharing&ouid=118296552415211719750&rtpof=true&sd=true)

[movies.csv](https://drive.google.com/file/d/13STkCnVnrstILuuTuqbh876Ri6pwt-sa/view?usp=sharing)

[users.csv](https://drive.google.com/file/d/10_oSOETgHXmQbe-mkZfv9-5Zzn_EN7ar/view?usp=sharing)
