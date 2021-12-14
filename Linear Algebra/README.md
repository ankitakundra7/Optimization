
## Question 1

A bank makes four kinds of loans to its customers and these loans yield the following annual interest rates to the bank:

• First mortgage 14%
• Second mortgage 20%
• Home improvement 20%

• Personal overdraft 10%

We are interested in the bank’s lending strategy. The information we know is as following:

1. In total $250 million is lent out.
2. First mortgages are 55% of all mortgages (i.e. first and second mortgage) issued.

3. Second mortgages are 25% of all loans issued.
4. The dollar-weighted average interest rate on all loans is 15%.

Calculate the lending strategy using matrix inversion.  How much is lent in home improvement loans?

 Answer in millions of dollars, rounded to 2 decimal places.  If the answer is $23080444.12, then you should enter 23.08.



## Question 2

Rankings are ubiquitous. You may have heard of Google’s PageRank and IMDB movie ratings. The backbone of these systems is Linear Algebra. We want to give you to taste of building your own ranking system to rank sports teams.

In a football league one is interested in modeling the ratings of teams based on the margin of victory and not just the outcomes, win/loss/draw. Consider the following data for five teams playing in such a league

Screen Shot 2020-08-12 at 11.19.30 AM.png

An entry (i, j) = (x-y) in this table represents a match between team i and team j where team i scored x points and team j scored y points. Our task is to first rate the teams and then convert the ratings to rankings.

Our goal is to find one number (the rating), ri,  for each team, so that when you compare the ratings between 2 teams, the difference in this rating is equal to the difference in points scored when those 2 teams played each other.  For example, team team 4 beat team 1 by a score of 38-7.  The point difference here is 31 points.  So if we compare team 4's rating to team 1's rating, r4 - r1 = 31.  This is not possible however because there are only 5 teams which leads to 5 values of r, and there were 10 games.  This means there are 5 unknowns and 10 equations, which is a system of equations that cannot be solved.  In this problem, our goal is to find the 5 unknowns that get as close as possible to satisfying the 10 equations!  To do this we will first pose the matrix equation with 5 unknowns and 10 equations and then use a trick from regression to find the closest answer possible.

 

We want

yk = ri − rj
Here yk is the difference in points scored by teams i, j in the match k and ri, rj are the ratings for teams i and j respectively. Assume N teams and M games.This won't be possible for every team/game, but the following steps will tell us how to find the best r's.

 

Part 1

Pose a matrix equation to solve for individual ratings of the form X r = y, the entries for coefficient matrix X represent the difference in ratings for the opponents in each game and y represents the difference in score of each game. Each row in X is a game between 2 teams.  This is the 5 unknown and 10 equation system.

Part 2

Typically the number of games is much greater than the number of teams, which means our system is overdetermined and we cannot solve the matrix equation by simply inverting the coefficient matrix. However, we can solve for approximate rating using least squares. Consider the normal equation for least squares of the form

X⊤X r = X⊤ y

If you don't know how to take matrix transpose in python, you can google it.
Let M = X⊤X. We can interpret the diagonal elements of M as the number of games played by a team and the off diagonal elements of the matrix M as the negation of the number of games played by team i against team j. Similarly the jth entry for the RHS p = X⊤y is the sum of the difference in points for every game played by team j.
Use the information above to determine the entries for M and X⊤y in our new system.

 

Part 3

The matrix M is not invertible. So you cannot solve for ratings, r by inverting M. However, to make it invertible you can add a constraint. For simplicity let us assume that all our ratings add to 0.

Modify your matrix equation Mr = p to incorporate this constraint and get a new system  

Mc r = pc.

To do this remove the last row in M and (X⊤ y) and replace it with an equation that guarantees all entries of r sum to 0.

Finally, solve for the ratings of the teams with data above and sort them to get team rankings.

 

Which team is the second best team?


## Question 3


A Lehmer matrix is one whose entries are specified by the following rule

Ai,j = i/j if j > i and Ai,j = j/i otherwise

Write a function named lehmer_entry which takes two arguments and outputs the value of the entry. Then use “for loop(s)” to generate a 20 by 20 Lehmer Matrix.

(Hint: First generate a 4 by 4 matrix with all the elements being 0. Then use for loop(s) and if statement to define the Lehmer matrix. Find the 4 by 4 Lehmer matrix and use the Wikipedia to check. Then you can change the code to run a 20 by 20)

Is A symmetric?

## Question 4

Going back to the Lehmer matrix problem.

 

Calculate the inverse of A and assign it to C.

Assign [1 2 3 4 5 6 7 8 9 10 10 9 8 7 6 5 4 3 2 1] to d.

Solve for x in the equation Ax = Cd

What is x10 ? Round to 1 decimal place.  Be careful if the answer you get is in scientific notation.
