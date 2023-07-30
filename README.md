# Movie-Metrics-Explorer


Overview
Movie-Metrics-Explorer is a project that involves SQL queries on the IMDb Top 250 Movies dataset. The dataset is represented in the IMDB_movies table, and it contains information about the top 250 movies based on user ratings on the IMDb platform. This project aims to explore various metrics and insights about these top-rated movies using SQL queries.

## Dataset
The IMDb Top 250 Movies dataset is stored in the IMDB_movies table, which has the following schema:
The columns in the table include:

1. Sl_No: A unique identifier for each movie.
2. Name: The name or title of the movie.
3. Release_Year: The year when the movie was released.
4. Duration: The duration of the movie in minutes.
5. Certificate: The certification or rating given to the movie (e.g., PG-13, R, etc.).
6. Rating: The average rating of the movie on IMDb, ranging from 0.0 to 10.0.
7. Votes: The total number of votes received by the movie on IMDb.
8. Director: The director(s) of the movie.
9. Stars: The main cast or stars of the movie.
10. Description: A brief description or plot summary of the movie.

## SQL Queries
The Movie-Metrics-Explorer project utilizes various SQL queries to analyze and explore the IMDb Top 250 Movies dataset. Each query serves a specific purpose and provides valuable insights into the dataset.

1. Retrieve the top 10 movies with all columns sorted by rating in descending order:

This query selects the top 10 movies from the IMDB_movies table, sorted by their rating in descending order. It retrieves all columns for these movies to get detailed information about each of them.

2. Find the movie with the highest rating:

This query identifies the movie with the highest rating among the IMDb Top 250 Movies. It retrieves all columns for this top-rated movie to understand its attributes.

3. Retrieve movies released in the year 2000 or later:

This query filters the IMDB_movies table to include only those movies that were released in the year 2000 or later. It helps in analyzing recent top-rated movies.

4. Get the total number of votes for each movie in descending order:

This query retrieves the names of the movies along with the total number of votes they received. The results are sorted in descending order based on the number of votes, giving insights into the popularity of each movie.

5.Find movies with a rating greater than 8 and release year after 2010:

This query selects movies from the IMDB_movies table that have a rating greater than 8 and were released after the year 2010. It helps identify highly rated recent movies.

6. Get the top 5 directors with the most movies in the top 250 list:

This query calculates the top 5 directors with the highest number of movies in the IMDb Top 250 list. It counts the number of movies directed by each director and orders the results accordingly.

7. Find the average rating of movies released in each decade:

This query calculates the average rating of movies released in each decade by grouping them based on their release year. The year is rounded to the nearest decade (e.g., 2001-2010), and the average rating is calculated for each group.

8. Retrieve the top 5 directors with the highest average movie ratings (consider directors with at least 3 movies in the dataset):

This query identifies the top 5 directors with the highest average movie ratings. It considers only those directors who have at least 3 movies in the IMDb Top 250 dataset. The average rating is calculated for each director, and the results are sorted in descending order.

9. Retrieve the names of the movies with the highest rating in each certificate category:

This query finds the movies with the highest rating in each certificate category. It groups the movies by certificate and selects the movie with the highest rating for each certificate, providing insights into the highest-rated movies for different age groups.

## Usage
You can use these SQL queries to explore and analyze the IMDb Top 250 Movies dataset. Simply run these queries on your favorite SQL database management system that supports the IMDB_movies table, and you will obtain various metrics and insights about the top-rated movies.

Happy exploring and analyzing! Feel free to utilize the results for further data visualization or research purposes. If you make improvements or add more analyses, consider contributing to this project on GitHub.

This README provides a comprehensive overview of the Movie-Metrics-Explorer project, explaining the dataset, SQL queries, and usage instructions. You can now upload this file to your GitHub repository to document and share your project with others.
