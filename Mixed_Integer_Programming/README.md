## Question 1

It costs a company $12 to purchase an hour of labor and $15 to purchase an hour of capital. If L hours of labor and K units of capital are available, then 0.05L2/3K1/3 machines can be produced. Suppose the company has $100,000 to purchase labor and capital. What is the maximum number of machines it can produce? Round to the nearest whole number of machines.


## Question 2

The file homework4stocks.csv  Download homework4stocks.csvcontains historical monthly returns for 27 companies. The first row contains stock names, and the first column contains the dates. For each company, calculate the estimated mean return and the estimated variance of return. Then calculate the estimated covariances between the companies' returns. Find a portfolio that achieves an expected monthly return of at least 1% and minimizes portfolio variance.  Assume no short selling is allowed. What is the portfolio's standard deviation?  Round to 2 decimal places?  Answer in terms of absolute numbers.  If your answer is 8% then you should enter 0.08.

 

We may or may not get to the content for this problem before it's due.  If we don't then don't worry about it.


## Question 3

The file variable_selection.csv  Download variable_selection.csvcontains observations of variables y, x1, x2, and x3. Here, y is the dependent variable. We want to choose a linear model that uses at most two independent variables such that the sum of squared residuals is minimized. This can be formulated as a constrained quadratic programming problem.

![Screen_Shot_2021-03-22_at_10.17.11_AM](Screen_Shot_2021-03-22_at_10.17.11_AM.png)

This is called best subset problem that is usually very hard to solve. We will solve this problem by enumeration. Run six OLS regressions (3 with one independent variable and three more with two variables each) and choose the regression that best fits the data. You can run each regression in R using the lm routine.

 

Which variables are included?


## Question 4

The file nflratings.csv  Download nflratings.csvcontains the results of 256 regular-season NFL games from the 2009 season. The teams are indexed 1 to 32 as shown below:

![Screen_Shot_2020-10-15_at_4.46.40_PM](Screen_Shot_2020-10-15_at_4.46.40_PM.png)

The csv data file contains a matrix with the following columns:

• Week (1-17)
• Home Team Index (1-32 from the table above)

• Visiting Team Index (1-32 from the table above)

• Home Team Score
• Visiting Team Score

For example, the first game in the matrix is team 25 Pittsburgh versus team 31 Tennessee, played at Pittsburgh. Pittsburgh won the game by a score of 13 to 10, and the point spread (home team score minus visitor team score) is 3. A positive point spread means that the home team won; a negative point spread indicates that the visiting team won.

The goal of this problem is to determine a set of ratings for the 32 NFL teams that most accurately predicts the actual outcomes of the games played, similar to homework 1. Here however, we will also incorporate a 'home field advantage' that adds some number of points to the predicted point spread.  Use NLP to find the ratings that best predict the actual point spreads observed. The model will estimate the home team advantage and the ratings.  The model accounts for the home team advantage by adding a constant (which you need to solve for) to the predicted point spread.  The objective is to minimize the sum of squared prediction errors. You will need to calculate the following:

• Actual Point Spread = Home Team Score – Visiting Team Score

• Predicted Spread = Home Team Rating – Visitor Team Rating + Home Team Advantage

• Prediction error = Actual Point Spread – Predicted Point Spread

Your goal is to minimize: Screen Shot 2021-03-22 at 10.22.05 AM.png  

You will also need to normalize the ratings (like you did in HW1). To do this, you set the actual average of the ratings to be 85 (this is somewhat arbitrary but based on the well-known Sagarin rating system). What do these ratings mean: If two teams had ratings of 82 and 91, then the second team would be predicted to win by 9 points if the game was played on a neutral field.

Formulate this as an NLP and solve it.

How many games (of the 256 played) does this model predict the winner correctly?
