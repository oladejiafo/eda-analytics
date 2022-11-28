# An Exploratory Data Analysis (EDA)

## Using Top 1000 Highest Grossing Hollywood Movies

### By - Oladeji Afolabi


## Overview

### About The Dataset
#### Context
This dataset contains information about the top 1000 highest grossing Hollywood movies. It is up to date as of 2021.

#### Acknowledgements
The data has been taken from Kaggle curtsey of SANJEET SINGH NAIK.

### Objectives
The objective of this analysis is to explore the trends in the highest rated Hollywood movies over the given year (1972 - 2021) 

-	What was the total revenue for each year and each category? 
-	What are the top 10 movies based on worldwide collections?
-	What is the average revenue in each genre over time?
-	How many films have been produced in each genre?

## Data Analytic Tool
Microsoft Excel was used throughout this analysis. Excel functions and features were put into use as well as the pivot table and pivot charts.

## Data Preparations & Processing

Initially, this was what the CSV data looks like
![image](https://user-images.githubusercontent.com/69392408/204203798-db51604d-77bd-4afd-a9d7-83dfb8b50442.png)

The dataset has the following column names: Title, Movie Info, Distributor, Release date, Domestic Sales (in $), International Sales (in $), World Sales (in $), Genre, Movie runtime and License.

## Data Cleaning & Formatting

The title had with it the year of the movie, there was release date with some dates missing, there was the genre (movie category) which has a list of categories for each movie. Also the movie duration was in hours and minutes.
To have a clearer access to each data item like year of production, month of production, specific genre and movie duration in a single unit, the following done to clean and format the dataset:
-	Movie titles were trimmed for possible extra spaces using the trim() function – [e.g “=trim(B2)” ]
-	The “Title” column was splitted into 2 columns “title_new” and “title_year” using the” Text to Column” feature in excel. 
-	Now the new column “title_year” has parenthesis () around it, so those were removed using the Search and Replace feature.
-	Similarly, 2 new columns were added to get the year and month of movie release from the “Release Date”, this was done using the YEAR(date) and MONTH(date) functions in these respective columns labeled “release_year” and “release_month”.
-	The “Genre” column was also splitted into columns using the “Text to Column” feature. The coma (,) delimiter was used to split these then the square bracket and the apostrophe around each new value in these columns were removed using search and replace.
-	Using the “Text to Column”, the “Movie Runtime” column was also splitted, then using a calculation, the value of the splitted hour and the minutes were converted into minutes only and labelled as “movie_minute_hr”.
-	Finally, the newly created “title_year” column was moved to be beside the “release_year” column for easy comparism.
-	All column names were converted to snake_case.
-	The release dates were converted to a uniform format.
-	A few movie titles were duplicated (like Aladdin & Lion King), but after carefully checking, there were only reproduced at different times.

Below is the outcome of the dataset cleaning and formatting.
![image](https://user-images.githubusercontent.com/69392408/204203968-a828f1ab-5763-46db-ac33-9af2e00fcd3c.png)

## Exploratory Data Analysis

Pivot table was used to create a number of analysis as illustrated below:

##### *Number of Movies per Genre, Showing Total Sales Revenue Across Markets*
 ![image](https://user-images.githubusercontent.com/69392408/204204315-87090e9a-4fb1-4345-a60a-6ab6bd582feb.png)

#### Observation:
-	The Action genre, the Adventure genre and the Comedy genre are the top selling movies and by correlation the highest in number available.

##### *10 Top Selling Movies World-Wide*
![image](https://user-images.githubusercontent.com/69392408/204204459-fa789a7e-0122-4ab6-8075-aa57e26d68dd.png)

#### Observation:
-	The Titanic has grossed the highest sales over time.

##### *Number of Movies Produced Each Year*
![image](https://user-images.githubusercontent.com/69392408/204204492-7a75f987-9f7a-42b4-8255-7797bdb28bd0.png)

#### Observation:
-	The years 2020 and 2021 has very low movie production. This is probably due to the corona virus.
-	Also of note is the fact that between year 2000 to 2019, the number of high selling movies were quite high as compared to the other years.

##### *Number of Movies Produced per Genre for Each Month in Trend*
![image](https://user-images.githubusercontent.com/69392408/204204612-0c38b8e8-1b00-4dee-87a3-bc3d460b49d7.png)

#### Observation:
-	There is no obvious correlation between the months movies are produced and the genre

##### *Average Revenue per Genre*
![image](https://user-images.githubusercontent.com/69392408/204204792-d5e72e10-851f-4359-bcdc-3a4d47f6c4c3.png)

#### Observation:
-	The categories, Mystery, Adventure and Action has the highest average revenues. 
-	Mystery category, despite not high numbers of production, notwithstanding have the highest average revenue.

##### *Total Revenue per Year*
![image](https://user-images.githubusercontent.com/69392408/204204852-d3d8ac56-076d-400f-8462-1d9a4a4e7a6a.png)

##### *Dynamic Dashboard*
Most of the above analysis were wrapped up into this interactive dashboard and filter enabled using the excel pivot table slicer.
![image](https://user-images.githubusercontent.com/69392408/204204938-985273e4-9818-48e0-87af-126be23cacf9.png)
