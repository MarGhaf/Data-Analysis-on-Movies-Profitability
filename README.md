# Data Analysis on Movie Profitability
![image](Image/nomadland.png)



**Authors:** Maryam Ghaffari
***

## Overview

Entertainment industry have been characterized by growth over the recent years. No doubt investment in this industry would be a smart strategy for big corporations to achieve their market share. However it is a high risk industry and it is affected by many complex factors, like movie quality, genre, leading actors, director, screenwriter, movie title, movie type, screen time, language, movie rating, release time, advertisement, production company, and distribution company. Microsoft have decided to create a new movie studio and they asked exploratory data analysis to help them to know what types of movies are most profitable

## Business Understanding

 Microsoft have decided to create a new movie studio, but they don’t know anything about creating movies. To run a new business, it is important to have an exploratory data analysis to understand the marketplace, set revenue and profitability goals. Exploring available database would help them to know what types of films are currently doing the best at the box office. In addition, other criteria like realse time and running time trend would help them to enhance their investment return guarantee.  
 The key business questions include:
 
    . Qestion 1; Which Generes need more budget and create gross more?
    
    . Qestion 2: Best relase month for geners and gross?
    
    . Qestion 3 : What is the perfect running time for a movie?


## Data Understanding and Analysis

The general research strategy in this project is to do exploratory data analysis on the persent data collection in film industry. The process include belwo steps:

 . Import libraries and load dataset
 
 . Data cleaning
 
 . Asking Analytical Questions and Visualizations
 
 . Conclusion & Recommendations
 
 
### Import libraries and load dataset

The first step to start a project is to choose neaded libraries and modulas in python and import them to your framework. For this project belwo libries were used:

Pandas: a software library written for the Python programming language used for data analysis and associated manipulation of tabular data in Dataframes
Numpy:  the core library for scientific computing in Python
Matplotlib: a comprehensive library for creating static, animated, and interactive visualizations in Python
Seaborn: a Python visualization library based on matplotlib. It provides a high-level interface for drawing attractive statistical graphics. 
OS: a module in Python provides functions for creating and removing a directory (folder), fetching its contents, changing and identifying the current directory.
Warnings :  a module suppresses repeated warnings from the same source to cut down on the annoyance of seeing the same message over and over.

There are 6 movie database in this project: 

1. bom.movie_gross.csv.gz

2. tn.movie_budgets.csv.gz

3. tmdb.movies.csv.gz

4. rt.movie_info.tsv.gz

5. rt.reviews.tsv.gz

6. im.db

These data collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) can be opened using  pd.read_csv () method, while the data from IMDB is located in a SQLite database and can asscess them with pd.read_sql() method. 


