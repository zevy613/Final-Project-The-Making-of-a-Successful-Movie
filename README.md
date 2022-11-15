# Final Project - Analysis of Movies

Author: William Borenstein


### Business problem:
For this project, I will produce a MySQL database on Movies from 2000 to 2019 from a subset of IMDB's publicly available dataset. Ultimately, I will use this database to analyze what makes a movie successful and will provide recommendations to the stakeholder on how to make a successful movie. This project will use a combination of machine-learning-model-based insights and hypothesis testing to extract insights for our stakeholders.

### Goal: 
 - Predict what makes a movie successful. 
 - Determine if the MPAA ratings (G, PG,...) of a movie affect how much revenue the movie generates.
 - Use a Linear Regression model to predict the revenue a movie will generate.

### Data
This data set is a conglomerate of different tables recovered from tbdm.com and imdb.com. This data set has 5,3019 rows and 25 columns. During my hypothesis test I will be focusing on movie rating. When modeling, the target column that I will try to predict is the total revenue a film is expected to generate. Some of the other key features of the data are budget, genres and popularity.

## Methodology
 - Part 1: Download several files from IMDB’s movie data set and filter out the subset of movies requested by the stakeholder.
 
 - Part 2: Use an API to extract box office revenue and profit data to add to the IMDB data
 
 - Part 3: Perform exploratory data analysis.
 
 - Part 4: Apply an E.T.L process on previously saved movie data. Construct and export a MySQL database using the extracted data, which includes preparing the data for a relational database.
 
 - Part 5: Apply hypothesis testing to explore what makes a movie successful.
 
 - Part 6: Produce a Linear Regression model to predict movie performance.

## Preliminary Data Exploration
Visual #1

![png](Visuals/heatmap.png)

From Visual #1 above we can see any features that strongly correlate with one another. From here we can see that budget and revenue, budget and view count and revenue and view count have strong correlations with each other. 


Visual #2

![png](Visuals/regplot_Budget-Revenue.png)

Above we can see the budget per movie and how much revenue that particular movie generated.


Visual #3

![png](Visuals/histogram_Movies-Category.png)

From this bar plot we can see how many movies there are in each movie rating that we pulled.


Visual #4

![png](Visuals/batplot_Revenue-Certification.png)

In this barplot we can see the amount of revenue based on movie rating.


## Hypothesis Testing
**Do some MPAA Ratings make more revenue than others?**

**Hypothesis**

- $H_0:$ The MPAA ratings have no effect how much revenue the movie generates.
- $H_1:$ The MPAA rating does effect how much revenue the movie makes.
 
 Data Type : Numeric (Revenue)
 
 Samples: More than 2 samples/groups
 
 Test: ANOVA and/or Tukey
 
 Assumptions: 
 
    - No significant outliers
    - Equal variance
    - Normality

**Outliers Removed**
 - Rating  R -> Number of outliers :  112
 - Rating  PG-13 -> Number of outliers :  80
 - Rating  UR -> Number of outliers :  28
 - Rating  PG -> Number of outliers :  37
 - Rating  G -> Number of outliers :  10
 - Rating  NC-17 -> Number of outliers :  2

**Normality Assumption**
 - We failed the test for normality. However, we can still proceed as planned because we have more then 15 samples in each group.


**Equal Variance**
 - Because we failed the test of equal variance we have to perform a Kruskal-Wallis test instead of a One Way ANOVA. 


**Final Conclusion**

    Test Results: KruskalResult(statistic=1764.3856914319545, pvalue=0.0)
Explanation: In this case we have a significant p-value which means we reject our null hypothesis and support our alternative hypthesis that "The MPAA rating does effect how much revenue the movie generates".


**A Post-Hoc** 

We can determined from a Post-Hoc Multiple Comparison Test that movies rated R, UR and NC-17 made significantly less in revenue than all other ratings. 

![png](Visuals/barplot_Tukeys_Data.png)

![png](Visuals/tukeys_plot_simultaneous.png)



## Other Hypotheses we can test for...
 - Q: Do movies that have longer movies earn more revenue than shorter ones?

 - Q3: Do movies released in particular years ern more or less then movies in other years?

 - Q: Do some movie genres earn more revenue than others?

## Regression Model-Based Insights

 - Finally I used a Linear Regression Model with the help of feature engineering and other machine learning models to predict movie revenue to extract insights and recommendations on what features of a movie are positive/negative predictors of success.
 
 
### Best Model

**QQ-Plot** (left) **Residual Plot** (right)

![png](Visuals/final_model_graphs.png)


**Final Training Scores**

![png](Visuals/final_model_results.png)


**Final Testing Scores**

 - r-square : is 0.723 
 - Mean Squared Error(MSE) : 3.343948e+15.

    
## Results
<!--  
![png](Visuals/)

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