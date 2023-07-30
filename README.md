# Movie-Metrics-Explorer

Movie-Metrics-Explorer
This project involves SQL queries on the IMDb Top 250 Movies dataset. The dataset is represented in the table IMDB_movies, with the following schema:

CREATE TABLE IMDB_movies(
   Sl_No        INTEGER  NOT NULL PRIMARY KEY 
  ,Name         VARCHAR(68) NOT NULL
  ,Release_Year INTEGER  NOT NULL
  ,Duration     INTEGER  NOT NULL
  ,Certificate  VARCHAR(3) NOT NULL
  ,Rating       NUMERIC(3,1) NOT NULL
  ,Votes        INTEGER  NOT NULL
  ,Director     VARCHAR(32) NOT NULL
  ,Stars        VARCHAR(62) NOT NULL
  ,Description  VARCHAR(239) NOT NULL
);
The queries used to explore the dataset are as follows:

Retrieve all columns for the top 10 movies in the table sorted by rating in descending order:



SELECT *
FROM IMDB_movies
ORDER BY Rating DESC
LIMIT 10;
Find the movie with the highest rating:


SELECT *
FROM IMDB_movies
ORDER BY Rating DESC
LIMIT 1;
Retrieve movies released in the year 2000 or later:


SELECT *
FROM IMDB_movies
WHERE Release_Year >= 2000;
Get the total number of votes for each movie in descending order:


SELECT Name, Votes
FROM IMDB_movies
ORDER BY Votes DESC;
Find movies with a rating greater than 8 and release year after 2010:


SELECT *
FROM IMDB_movies
WHERE Rating > 8 AND Release_Year > 2010;
Get the top 5 directors with the most movies in the top 250 list:


SELECT Director, COUNT(*) AS NumMovies
FROM IMDB_movies
GROUP BY Director
ORDER BY NumMovies DESC
LIMIT 5;
Find the average rating of movies released in each decade:


SELECT (Release_Year / 10) * 10 AS Decade, AVG(Rating) AS AverageRating
FROM IMDB_movies
GROUP BY Decade
ORDER BY Decade;
Retrieve the top 5 directors with the highest average movie ratings (consider directors with at least 3 movies in the dataset):


SELECT Director, AVG(Rating) AS AvgRating
FROM IMDB_movies
WHERE Director IN (
    SELECT Director
    FROM IMDB_movies
    GROUP BY Director
    HAVING COUNT(*) >= 3
)
GROUP BY Director
ORDER BY AvgRating DESC
LIMIT 5;
Retrieve the names of the movies with the highest rating in each certificate category:


SELECT Certificate, Name, Rating
FROM IMDB_movies AS m1
WHERE (Certificate, Rating) IN (
    SELECT Certificate, MAX(Rating) AS MaxRating
    FROM IMDB_movies AS m2
    WHERE m1.Certificate = m2.Certificate
    GROUP BY Certificate
);
These SQL queries provide valuable insights into the IMDb Top 250 Movies dataset, such as top-rated movies, top directors, average ratings per decade, etc. The results obtained from these queries can be used for further analysis and exploration of the dataset.

Feel free to use this README file to document and share your Movie-Metrics-Explorer project on GitHub. Happy coding!
