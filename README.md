# MovieRecommendationSystem
Movie Recommendation System using matrix factorization. Recommending top 10 movies for a user, according to the bunch of users tastes for movies

How to Run the File:
1)	In the cell no:1 of the code, there is automatic download of dataset file. If that doesn't work on your system. please go to         https://files.grouplens.org/datasets/movielens/ml-20m.zip and download the zip file and place this python file one level before the dataset folder and run it.
Example: A folder containing ipynb file and an unzipped folder of data set file.
2)	At cell no:2, please give the input for getting the subset of dataset.
3)	At cell no:9 in the code, please give No: of iterations, user id and K values.

Matrix Factorization Algo-Approach:
•	First, we will take the input R matrix from the dataset and calculate the userFeature matrix and ItemFeature matrix using random NumPy array.
•	Next, we will find the error rate for each element by iterating through every element of input matrix and subtracting the original value with the product of UserFeatures and ItemFeatures at (m, n) location. 
•	Now, we will use a method called gradient descent to minimize the error rate. 
•	From the gradient, the mathematic formula can be updated for both userFeature and ItemFeature. 
•	From the above equation, userFeatures and itemFeatures can both be updated through iterations until the error converges to its minimum. 
•	When we get the final result, all the values which are zero in input matrix will be filled with recommended ratings.

Apply matrix factorization to the dataset:
•	First, we will take ratings.csv file and movies.csv file from the MovieLens dataset and form dataframe and apply the filters to extract the data according to the limits provided by the user.
•	After getting the ratings dataframe we will convert the dataframe to 2D numpy array as its needed for matrix factorization fuction.
•	As we have Input 2D matrix, we will give the matrix as input to the matrix factorization function and calculate the recommended ratings.
•	Now, with every input, we will get the ratings of requested user and sort them in descending order of their predicted ratings and show the top 10 movie recommendations to the user.
•	Now, we will get the list of rated movies movie positions per user and store them for future use.
•	With the help rated movies movie positions, we will get the ratings of input and ratings of predicted for those positions and calculate the accuracy of my recommendation system.
