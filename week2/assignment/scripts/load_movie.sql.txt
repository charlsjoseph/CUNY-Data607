DROP TABLE IF EXISTS movies;

CREATE TABLE movies 
(
  movie_id int NOT NULL,
  movie_name varchar(50) NOT NULL,
  movie_type varchar(20) NOT NULL,
  year int NULL
);


LOAD DATA  INFILE 'C:/data/movies.csv' 
INTO TABLE movies
FIELDS TERMINATED BY ',' 
LINES TERMINATED BY '\n'
(movie_id, movie_name, movie_type,year);

SELECT * FROM movies;
SELECT COUNT(*) FROM movies;

