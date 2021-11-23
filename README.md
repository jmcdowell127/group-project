# Blockbuster and Critically Acclaimed Movies
![1 -Blockbuster-Movie-Night-1](https://user-images.githubusercontent.com/85372441/142780435-602e541a-5dba-45f3-bd2d-bb13f1acaaff.png)


## Overview of Presentation


[Google Slides Presentation](https://docs.google.com/presentation/d/1NvvILCPFJwhJ9YsGHEij6EZMNrbiN6z8T5EJUJ1asY0/edit#slide=id.g1033fb929ec_2_77)


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
5.	Created two classification algorithms to identify whether a movie is a hit based off of: 
    * Profitability
    * Metascore

### Questions we hope to answer with this analysis
1. Is a movie a hit based on it's metascore?
2. Is a movie a hit based on how much money was grossed?
3. Will a movie be a hit depending on season of the year it was released?

### Data Exploration
In this phase of our project we created a SQLite database to easily navigate and filter the data to see how we could utilize this data for our project, we then used the online Entity Relationsip Diagram(ERD) to begin exploring the data. We then created tables we thought would be useful once we got to analyzing the dataset. 


<img width="371" alt="erd" src="https://user-images.githubusercontent.com/85372441/142781480-32405278-fc3b-49e7-9da3-0df0cf4b1c3d.png">

<img width="572" alt="sqlite" src="https://user-images.githubusercontent.com/85372441/142781535-2b0af52c-aa2e-4675-b149-944922599407.png">

<img width="795" alt="database" src="https://user-images.githubusercontent.com/85372441/142781545-9e353dca-d012-4518-b831-bf23d2ad0f68.png">


### Data Analyis
After reviewing the data in our database we noticed that there are strong correlations between a few columns. Those columns were budget, total_gross, critic and user reviews (which determine metascore). From this we began to create logistic regression machine learning models in attempt to accurately predict whether a movie will be a hit.

<img width="356" alt="hmap" src="https://user-images.githubusercontent.com/85372441/142782823-06f36010-cad1-4f4d-a883-8f44a953e187.png">


## Machine Learning (Logistic Regression)
Preproccessed the data by removing unnecessary columns, then created three new columns (gross_profit, blockbuster, and meta_hit) by creating the following classification algorithms:
* <img width="548" alt="grossProfit" src="https://user-images.githubusercontent.com/85372441/142783163-2f1b52e7-8f48-4c0a-8fc2-020f3932bf50.png">
* <img width="566" alt="blockbuster" src="https://user-images.githubusercontent.com/85372441/142783167-8a386a66-57ac-4cc5-8210-1ddd059625a8.png">
* <img width="274" alt="metaHit" src="https://user-images.githubusercontent.com/85372441/142783180-1ea6a061-9b8b-4315-8ea5-f78aabbf111b.png">


The decision to create a gross profit column was to be able to include both lower and higher budget movies that still had a high profitablity. We then decided to create two seperate logistic regression models, one for critically acclaimed movies which we describe as a meta_hit and a second for blockbuster movies which had high profit margins.
We decided on logistic regression models because our target outcome is binary and this model method is best suited for binary outcomes. The limitations in our models came when predicting whether a movie would be a 'meta_hit'. The metascore model was able to highly predict whether it would __not__ be a hit but was limited when predicting whether it would be a hit. Even though it had lower scores in that aspect, being able to have a high accuracy in predicting whether it would not be a hit is more than suffice since a director or producer in the future will know if their movie will __not__ be critically acclaimed.

### Logistic Regression Results
__Critically Acclaimed (meta_hit)__


<img width="448" alt="meta_scores" src="https://user-images.githubusercontent.com/85372441/142783573-d7f75a88-dc48-4f68-b81c-78774d412606.png">


__Blockbuster__


<img width="354" alt="bbscores" src="https://user-images.githubusercontent.com/85372441/142783721-32d8a6c5-2b37-48d4-9101-a262584aab44.png">


* The model based off of meeting the meta hit requirements had an accuracy of __88%__.
* The model based off of meeting the blockbuster requirements had an accuracy of __97%__.

## Tableau Dashboard
[Tableau Visualizations](https://public.tableau.com/app/profile/jeremy.ocain/viz/moviedatav3/WhatmakesaHitMovie?publish=yes)


<img width="554" alt="tab" src="https://user-images.githubusercontent.com/85372441/142784007-7156fd29-c6e8-4c45-92e9-baf3ece743f4.png">


<img width="569" alt="tab2" src="https://user-images.githubusercontent.com/85372441/142784020-0b215edb-18c9-4f9a-b4b0-7efb3c0c1fcc.png">


<img width="544" alt="tab3" src="https://user-images.githubusercontent.com/85372441/142784021-bdbb7913-17b4-430b-a38b-5e971a3c8cab.png">

