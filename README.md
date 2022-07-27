# Data Analysis on Movie Profitability
![image](Image/nomadland.png)





## Overview

Entertainment industry have been characterized by growth over the recent years. No doubt investment in this industry would be a smart strategy for big corporations to achieve their market share. However it is a high risk industry and it is affected by many complex factors, like movie quality, genre, leading actors, director, screenwriter, movie title, movie type, screen time, language, movie rating, release time, advertisement, production company, and distribution company. Microsoft have decided to create a new movie studio and they asked exploratory data analysis to help them to know what types of movies are most profitable

## Business Understanding

 Microsoft have decided to create a new movie studio, but they don’t know anything about creating movies. To run a new business, it is important to have an exploratory data analysis to understand the marketplace, set revenue and profitability goals. Exploring available database would help them to know what types of films are currently doing the best at the box office. In addition, considering other criteria like realse time and running time trend enhances the likelihood of a descent return on their investment. 
 The key business questions include:
 
    - Qestion 1; Which Generes need more budget and create gross more?
    
    - Qestion 2; What is the best months for releasing a movie?
    
    - Qestion 3; What is the perfect running time for a movie?


## Data Understanding and Analysis

The general research strategy in this project is to do exploratory data analysis on the present data collection in the film industry. The process includes the below steps:

 - Import libraries and load dataset
 
 - Data cleaning
 
 - Asking Analytical Questions and Visualizations
 
 - Conclusion & Recommendations
 
 
### Import libraries and load dataset

The first step to start a project is to choose neaded libraries and modulas in python and import them to your framework. For this project belwo libries were used:

- `Pandas`: a software library written for the Python programming language used for data analysis and associated manipulation of tabular data in Dataframes

- `Numpy`:  the core library for scientific computing in Python

- `Matplotlib`: a comprehensive library for creating static, animated, and interactive visualizations in Python

- `Seaborn`: a Python visualization library based on matplotlib. It provides a high-level interface for drawing attractive statistical graphics. 

- `OS`: a module in Python provides functions for creating and removing a directory (folder), fetching its contents, changing and identifying the current directory.

- `Warnings` :  a module suppresses repeated warnings from the same source to cut down on the annoyance of seeing the same message over and over.

There are 6 movie databases in this project: 

1. bom.movie_gross.csv.gz

2. tn.movie_budgets.csv.gz

3. tmdb.movies.csv.gz

4. rt.movie_info.tsv.gz

5. rt.reviews.tsv.gz

6. im.db

These data collected from various locations and the different files have different formats. Some are compressed CSV (comma-separated values) can be opened using  `pd.read_csv()` method, while the data from IMDB is located in a SQLite database and can asscess them with `pd.read_sql()` method. 

## Data cleaning
The second step in doing a project is to cleaning up datasets and making them operational. In fact, this step in acquiring and cleaning data is 80% of the work. In this way, dealing with messy data means dealing with missing values, inconsistent formatting, malformed records, or nonsensical outliers. The begining of data cleaning is to print a concise summary of a DataFrame with `.info()` method and view a small sample of DataFrame object with `.head()` method. Through the `.info()` method we access the valuable information about missing values and datatype. `.isnull()` is a method that help us to determin the missing value and based on the percentage of them or necessity of them, decided on delet (`.dropna()` method) them or fill (`.fillna()` method) them with sutiable values. With duplicated() method we also the duplication and drop them through `.drop_duplicates()` method. 

Data in wrong format can make it difficult, or even impossible, to analyze data. `.to_datetime()` and `.astype()` were two methods we used to change the data type. In some cells we had wrong data and changed them with `.replace()` method. 
 
Sometimes we need to updates the content of several DataFrame by merging them together (`.merge()` method. Selecting type of merge and the common coulnm to merge on it change the new datafram structure.  

## Asking Analytical Questions and Visualizations

Asking the right data analysis questions is crucial for getting accurate, actionable insights from the data analytics. In this project we answer to three main questions.
## Question 1;  Which Genres need more budget and create more gross?

To answer to this question, movies were categorized based on their genres. Then their production budget and worldwide gross plot based on genres. 

### Genre Visualisation

![image](https://user-images.githubusercontent.com/101681195/181303372-10969a94-68b6-4a97-8389-46a1995a7aed.png)

### Net Income Visualisation

![image](https://user-images.githubusercontent.com/101681195/181303427-54db0d48-6774-474a-9d32-26a448ee592b.png)

### Budget Range Visualisation

![image](https://user-images.githubusercontent.com/101681195/181303477-6d499b5b-e754-4665-951e-2b55a5fd3f20.png)

### Insights
According to 'Genre Visualisation' fiure, sci-Fi, adventure, action and animation genres had the most worldwide gross while western, family, thriller and music genres had less worldwide gross. This fig showed higher gross did not necessary need higher production budget. To better understanding the relationship between production budget and worldwide gross, net income was plotted (Net Income Visualisation). Net income defined as worldwide gross minus production budget. The plot showed movies net income based on their genres.  Sci-fi, adventure, musical, animation and action genres ranked one to five. The net income of sci-fi genres is around 300 million dollars which is about two time more than other 4 top genres. 

By Categorizing the budget deciding on choosing the genres based on the amount of budget is more logical. According to 'Budget Range Visualisation', higher than 344 million dollars sci-fi genres had more gross while for budget less than 263 million dollars drama genres created more gross. 
### Recommendation
- Make a sci-fi film with a production budget between 344-425 million dollars.
- Make a drama movie with production budget between 182-263 million dollars. 

### Future work
 - Explore the effect of directors, producers and writers on gross

## Question 2; What is the best months for releasing a movie?

Releasing time of the movies is one of the factors that have affect on movie gross

### Release Time Visualisation

![image](https://user-images.githubusercontent.com/101681195/181303542-2bb47204-23e1-40cb-a17c-e8b2e49b0cd5.png)

### Release Time by Gener Visualisation

![image](https://user-images.githubusercontent.com/101681195/181303608-63abe8c2-b319-44b3-8722-d5a07efd72d7.png)

### Insights

According to the 'Release Time Visualisation' figure, releasing movies in Jun, July and May produced more worldwide gross. That showed at the beginning of summer is a suitable time for the movie release. On the other hand, September, October, and January were not the appropriate time for the movie release. But before deciding just on this plot we should check genre diversity each month. By taking a look at the number of movies released each month among high gross genres (Sci-Fi, Adventure, Action, and Animation) that showed in the 'Release Time by Gener Visualisation' figure it is clear that the number of the movies had an almost similar trend in every month. This plot confirmed the impact of releasing time on movie gross. 

### Recommendation
- The best month for releasing movie is beginning of the summer in July and the worst time is in September

### Future work
- Studying on the best gap between the movie trailer release and movie relase time

## Question 3; What is the perfect running time for a movie? 

### Running Time Visualisation
![image](https://user-images.githubusercontent.com/101681195/181303663-1bfb21d9-3a10-48c8-8b05-43db071725b6.png)

### Running Time by Gener Visualisation
![image](https://user-images.githubusercontent.com/101681195/181303721-8a646f6a-7915-4c84-b67c-479c4311b806.png)

### Insights
Normally we assume the low-budget movies are shorter. But according to the  'Running Time Visualisation' figure, running time did not cause a trend in increasing the movie budget. On the other hand, the longer movie did not result in higher gross. It seems movies with 70-90 minutes running time had higher gross.  
Among the top 100 high-gross movies, most action genres had running times between 110-150 minutes. Adventure movies had various running times from 90 minutes to 170 minutes, and higher running times did not enhance the gross. Sci-fi with a running time between 90-110 had a higher world gross. It is hard to conclude that each genre with what running time had a higher gross. 

### Recommendation
- Make movie with running time between 70-90 min. 

### Future work
- Studying on effect of running time on reducing the cinemas showtimes and its impact on box office performance. 
