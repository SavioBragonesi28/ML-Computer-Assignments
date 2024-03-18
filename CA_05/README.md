# CA05 – kNN-based Movie Recommender Engine

## The Application
At scale, this would look like recommending products on Amazon, articles on Medium, movies on Netflix, or videos on YouTube. Although, we can be certain they all use more efficient means of making recommendations due to the enormous volume of data they process. However, we could replicate one of these recommender systems on a smaller scale using what we have learned here in this article. Let us build the core of a movie recommender system.

### What question are we trying to answer?
Given a movie dataset, what are the 5 most similar movies to a movie query?

## Part 1: Data Importing and EDA
For this part, we loaded the data, performed some basic EDA, and dropped the "label" column since it was composed of only zeros.

## Part 2: Building the Model
We started by splitting the numerical and non-numerical columns from our dataset. Then, we imported kNN, set the number of neighbors to 5, and fitted our data into the model.

## Part 3: Using the Model
Using the information given, we created an array with the information of the new movie, and we used `kneighbors` to find the names of the most similar movies:
- 12 Years a Slave
- Hacksaw Ridge
- Queen of Katwe
- The Wind Rises
- A Beautiful Mind

## Acknowledgments
-Team 07
-Dr. Brahma
