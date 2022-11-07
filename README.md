# Final Project - Analysis of Movies

Author: William Borenstein


### Business problem:
For this project, I will produce a MySQL database on Movies from 2000 to 2019 from a subset of IMDB's publicly available dataset. Ultimately, I will use this database to analyze what makes a movie successful and will provide recommendations to the stakeholder on how to make a successful movie.

### Goal: 
 - Predict what makes a movie successful. 
 - Determine if the MPAA ratings (G, PG,...) of a movie affect how much revenue the movie generates.
 - Use a Linear Regression model to predict the revenue a movie will generate.

### Data
This data set is a conglomerate of different tables recovered from tbdm.com and imdb.com. This data set has 5,3019 rows and 25 columns. During my hypothesis test I will be focusing on the movies rating. When modeling, the target column that I will try to predict is revenue. Some of the other key features are budget, genres and popularity.

## Methodology
 - Part 1: Download several files from IMDB’s movie data set and filter out the subset of movies requested by the stakeholder.
 
 - Part 2: Use an API to extract box office revenue and profit data to add to the IMDB data
 
 - Part 3: Perform exploratory data analysis.
 
 - Part 4: Apply an E.T.L process on previously saved movie data. Construct and export a MySQL database using the extracted data, which includes preparing the data for a relational database.
 
 - Part 5: Apply hypothesis testing to explore what makes a movie successful.
 
 - Part 6: Produce a Linear Regression model to predict movie performance.

## Results
Visual #1

![png](Visuals\heatmap.png)

<!-- From Visual #1 above we can see that as a patient gets older thier chances of getting heart disease increase. 


Visual #2

![image](https://user-images.githubusercontent.com/54513705/192051282-cfd23be0-4b24-4efb-8b6a-52a04bb9f519.png)

From Visual #2 above we can see that people who are asymptomatic in regards to chest pain, are more at risk. This makes sense because people who don't have any symptomes don't know that there is a problem that needs to be addressed. As a result, no preventative measures are taken which leads to a higher rate of positivity. One way to avoid this is have regular check ups and frequent testing.

## Model
The final classification model that I would put in production is K-Nearest Neighbors Classifier.
       
-------------------Testing Data Scores-------------------
  
  Accuracy score :  0.878
  
  Recall score :  0.886
  
  Precision score :  0.9

The reason I chose this model was because it has the highest recall score which minamizes the number of false negatives.

## Recomondations:
I think that if more data was collected, better results could have been achieved. Specifically the samples between male and female patients could have been more even balanced. Secondly, there could have been more features so the model could be more informative.

## Limitations & Next Steps: 
One way we could enhance this model would be to add more hyper-parameter tuning on more variables. Also, other Feature Engineering could have been performed with more knowledge of the subject matter. An expert could be consulted on which what features can be modified for better results. Lastly, a more or less accurate percentage of variance could have been chosen when using PCA. Agian, a subject matter expert can be consulted for guidence.


## For further information 
zevy613@gmail.com
 -->