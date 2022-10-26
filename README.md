# group_8_capstone


## overview:
1. Business Understanding
2. Data Understanding and Analysis
3. Code Overview
4. Statistical Communication
5. Conclusion



#### Business Understanding


To companies who decided to create a new movie studio, showing:
    How much can you expect to gross domestically and globally?
    What are the most popular genres from 2010 to 2018?
    What movie genre will offer the most advantageous entry point into the market?



#### Data Understanding and Analysis


There are 6 data given initially, but only utilized 3

bom.movie_gross.csv.gz is csv zipped file. Using names of movie, combine the data with movie rating table from im.db file. This combines the rating tables with domestic gross and studio datas.

im.db.zip is database file. Utilize sqlite3 to open and organize the data which allows to work on necessary information (movie ratings table)

tn.movie_budgets.csv.gz is csv zipped file. Using names of movie, combine the data with movie rating table from im.db file. This combines the rating table with production budget to movie rating table. 


After combining all datas with movie rating table using merge, organized the data

From the movie rating table, drop rows with null values in genres, studio, and domestic gross columns since they are categorical data which is hard to replace. 
Also, the null values are only a small portion of the entire data, so it is trivial number. Since domestic gross and production budget is most important information that used durig visualization, null values has to be dropped, but we kept the zero values for accuracy.
From the production budget, domestic gross and worldwide gross columns, dollar symbols and other special characters are removed and converted to integer number

From the movie rating table, drop the foreign gross column since it is not used.



#### Code Overview

###### visualization 1:

The first visualization display the relationship between production budget and gross for both domestic and worldwide
With the organized data, movie rating, draw box plot that display the minimum, maximum, median, 25 and 75 percent percentile, and outliers. For more percisive reference, also draw the box plot without outliers.

With the visual reference, identify that there is a linear relationship between production budget and gross for both domestic and worldwide. 

For final visualization, draw the scatter plot for each domestic gross and worldwide gross with production budget. Gross is y axis, and budget is x axis. Use units in million dollars for user-friendly purpose.
Along with the scatter plot, draw the line of best fit to show the relationship between gross and production budget.

From the domestic gross and production budget plot, it is showed that there is a strong statistical relationship between production budget and gross revenue. 


https://github.com/wokehusker/group_8_capstone/blob/main/visualization_1.ipynb



###### visualization 2:

In this document, we created 4 different charts utilizing our custom dataset: df_gross.zip

The first visualization we created shows us the top 10 movie genres most produced from our dataset from 2010 to 2018. For this, we grouped each of the genres together and took the total count of different movies within that genre. We then listed it in ascending order to see which genres were produced the most. 

Our second visualization then took those top genres and looked at how much money each was earning over the span of 8 years. We pulled out those genres from the dataframe, listed them, and listed their total domestic gross. From this chart we could understand which genres were going to see the most profit and cross reference it to the first visualization to see where we should be targeting. 

The third visualization was determined by the genre we thought had the most room for a profitable movie. This genre was “Action, Adventure, Fantasy” Movies. We filtered out movies only in this genre, took a count of how many movies were produced per year, and then graphed it using a bar graph. 

Our final visualization is a duplicate of the third where the only difference was that instead of looking at “Action, Adventure, Fantasy” we looked at “Action, Crime, Drama” Movies.


https://github.com/wokehusker/group_8_capstone/blob/main/visualization_2.ipynb


###### visualization 3:

The third visualization display the relationship between the studio and the market share.
With the cleaned data, group them by studio in order to get the sum of domestic gross for each studio.
Using the total domestic market, by adding all domestic gross of every studio, find the market share of each studio.
For user-friendly purpose use percent instead of actual values.
Since top 20 studios have 97.2 percent of entire market share, only display top 20 studios.
Using bar plot, use studio as x axis and percent for y axis.
From the result, notes that BV is part of Disney, WB is Warners Brothers, Uni is Universial Studio, Par. is Paramount Pictures.



https://github.com/wokehusker/group_8_capstone/blob/main/visualization_3.ipynb



#### Statistical Communication



#### Conclusion

Based on our research conducted, we believe that the genres of "Action, Adventure, Fantasy" and "Action, Crime, Drama" offer the best opportunity to successfully break into the film industry. 

From here some of the next steps would include:

<br />Selecting a genre for the movie

<br /><br />Generating a storyline and script, while conducting market research on the ideas

<br />Setting a prodution budget and research successful directors and actors/actresses

<br />Producing the movie

<br />Conducting research on the best method of release (Theaters, Streaming platforms, TV, etc.)


#### Resources
used zip files in 
https://github.com/wokehusker/group_8_capstone/blob/main/zippedData/bom.movie_gross.csv.gz
https://github.com/wokehusker/group_8_capstone/blob/main/zippedData/rt.movie_info.tsv.gz
https://github.com/wokehusker/group_8_capstone/blob/main/zippedData/rt.reviews.tsv.gz
https://github.com/wokehusker/group_8_capstone/blob/main/zippedData/tmdb.movies.csv.gz
https://github.com/wokehusker/group_8_capstone/blob/main/zippedData/tn.movie_budgets.csv.gz

modified data files in
https://github.com/wokehusker/group_8_capstone/blob/main/df_gross.zip
https://github.com/wokehusker/group_8_capstone/blob/main/df_rating.zip

more information in
https://github.com/learn-co-curriculum/dsc-ai-academy-semester1-capstone


