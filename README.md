# Blockbuster and Critically Acclaimed Movies
![1 -Blockbuster-Movie-Night-1](https://user-images.githubusercontent.com/85372441/142780435-602e541a-5dba-45f3-bd2d-bb13f1acaaff.png)

[Google Slides Presentation](https://docs.google.com/presentation/d/1ffu_9Blp36GUOre-hPolBHvnzBkT2dG2YVnBj6VuBTc/edit#slide=id.gfa7f642fd3_0_15)


[Tableau Visualizations](https://public.tableau.com/app/profile/jeremy.ocain/viz/moviedatav3/WhatmakesaHitMovie?publish=yes)

## Overview of Presentation
### Topic
Movies are mostly considered to be a 'hit' based off of two criteria; whether the movie is a blockbuster and profited generously or if the movie is loved by the critics and is awarded high rating scores. In this analysis our group decided to dive into both of these criteria and accurately predict whether a movie will be a 'hit' in the future.

### Reason
As a group we are all fans of movies and are curious to see what really effects whether a movie will be successful or not.

### Questions we are looking to answer with this analysis
* Is a movie a hit based on simply Metascore, Gross Income or a mixture of these outputs?
* Is there a seasonality effect in place?
* Does higher budget increase hit probability?
* Has there been a significant change in profitability for movies over the decades analyzed?
* Is there any correlation by genres?

### Resources utilized:
1.	CSV file from Kaggle - [IMDb movies.csv](https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+movies.csv "IMDb movies extensive dataset")
2.	Pandas / Python / Sqlalchemy / Scikit-learn / Seaborn
3.	SQLite to clean and integrate data
4.	Tableau for visualizations and final presentation

### Questions we hope to answer with this analysis
1. Is a movie a hit based on it's metascore?
2. Is a movie a hit based on how much money was grossed?
3. Will a movie be a hit depending on season of the year it was released?

### Data Exploration
In this phase of our project we created a SQLite database to easily navigate and filter the data to see how we could utilize this data for our project, we then used the online Entity Relationsip Diagram(ERD) to begin exploring the data. We then created tables we thought would be useful once we got to analyzing the dataset. 


<img width="371" alt="erd" src="https://user-images.githubusercontent.com/85372441/142781480-32405278-fc3b-49e7-9da3-0df0cf4b1c3d.png">

<img width="572" alt="sqlite" src="https://user-images.githubusercontent.com/85372441/142781535-2b0af52c-aa2e-4675-b149-944922599407.png">

<img width="795" alt="database" src="https://user-images.githubusercontent.com/85372441/142781545-9e353dca-d012-4518-b831-bf23d2ad0f68.png">


### Data Analyis (Logistic Regression)

