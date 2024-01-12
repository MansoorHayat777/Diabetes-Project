# Diabetes
Using Jupyter Notebook to clean, visualize and predict diabetes outcome

I have a real interest in chronic diseases for both professional and personal reasons, and I wanted to play around with some real world data to work and improve upon some of my python skills, so I started by downloading the data from kaggle (https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database), and I have it loaded here on Github for easy download along with my python notbook file

I opened my Jupyter Notebook from the Anaconda Navigator and imported the relevant libraries I would be working with:
  
I then read the data into a dataframe and looked at the head and tail data (first 5 observations and final 5 obeservations) to see what I was working with

I wanted to play around with some other ways to though the data, so I also displayed a random sample of 10 records

Next, I wanted to check out the number of observations and the column types and names just to see how many columns I had and what type of formats they were.  It was a pretty simple file with expected types, so now we need to look into the data to see what we're working with.

The first step I took was to get a summary of the descriptive stats.  Given that we have some minimum values that were zero, I decided to clean the data next.

I started this by looking for any null values or duplicates in the data.  There were no duplicates, so I moved on to the missing values.  I printed off the number of null values for each of my relevant numerical variables.  There are really two directions you can go with null values; you can either remove any variables with missing values, or you can impute the missing values using the mean, which is what I ended up doing. 

I used the describe function to look back at the summary statistics and we had achieved our goal.

Now it's time to visualize.  I looked at a plot of the counts for the outcome (diabetes) using both a pie chart and a column chart and then I wanted to get an idea of the distribution by graphing histograms against the response variables.  Next step was to look at the relationship between the independent variable and the dependent variables, so I ran a scatter polot matrix to view them all at once.  You can also do this by plotting a heat map of the correlations, which is included in the code.

We can see that there are some highly correlated variables to the outcome, so that will be something to watch as we build our models.

Next, I applied a standard scaler using sklearn and then split the data into training and testing data.

After I had the data prepped and ready, I used the training model to train three different models: 1) Logistic regression, 2) Decision Tree, and 3) Random Forest.  After training the model, I used the test data to look at how well the model worked.  The Decision Tree and Random Forest both had a slightly higher accuracy than Logistc Regression, but all were not too bad, hovering around 80%.  Of course, that is not the only thing important for reviewing a model's performance, so I ran a confusion matrix for each model to look at recall, specificity, precision, and f1-score.

It was a pretty fun and easy dataset to work with, and it gave me an opportunity to begin working more on my coding.


  
