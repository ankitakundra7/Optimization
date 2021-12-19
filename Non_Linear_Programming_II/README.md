## Question 1

The following csv file ( hw5data.csv  Download hw5data.csv ) has data that we will use to help define an objective function.  The columns in the file are w1, w2, w3.  We want to pick x, y, and z to minimize

f(x,y,z)=\frac{1}{n} \sum_{i=1}^n \exp \left( x w_{1i} +y w_{2i} \right) ( z-w_{3i})^2

To help with the calculus I will tell you the derivative of each summand with respect to x, y, z.

\frac{\partial f_i}{\partial y}=w_{i}\exp \left( x w_{1i} +y w_{2i} \right) ( z-w_{3i})^2

\frac{\partial f_i}{\partial y}=w_{2i}\exp \left( x w_{1i} +y w_{2i} \right) ( z-w_{3i})^2

\frac{\partial f_i}{\partial y}=2exp \left( x w_{1i} +y w_{2i} \right) ( z-w_{3i})


where fi is the i'th element of the objective function sum.


Start with an initial guess of x,y,z = 0 and run 50000 epochs of gradient descent with a step size of 1e-3.  This will be used as our base case solution.  What is the optimal objective value? Round to 3 decimal places.


## Question 2

Now use stochastic gradient descent to solve this problem.  Set your batch size to be 10 (number of data points in each batch...not the total number of batches).  Run 100 epochs, starting at an initial guess of x,y,z=0.  Before your outer-most for loop set your seed to be 4382 by running np.random.seed(4382) so that everyone gets the same answer!

What is the objective now?


## Question 3

Now use ADAM with the usual parameters, and set your seed to 11492.  How many epochs are required to get 3 digits of accuracy, with respect to the solution to the first problem?


