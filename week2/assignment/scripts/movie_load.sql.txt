DROP TABLE IF EXISTS movie_ratings;

CREATE TABLE movie_ratings 
(
  movie_id int NOT NULL,
  viewer_name varchar(20) NOT NULL,
  rating int NULL
);

SELECT * FROM movie_ratings;

LOAD DATA  INFILE 'C:/data/movie-rating2.csv' 
INTO TABLE movie_ratings
FIELDS TERMINATED BY ',' 
LINES TERMINATED BY '\n'
(movie_id, viewer_name, @rating)
SET
rating = nullif(@rating,-1);


SELECT * FROM movie_ratings ;
SELECT COUNT(*) FROM movie_ratings;

