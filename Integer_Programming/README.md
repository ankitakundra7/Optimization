## Question 2

A company is thinking about building new facilities in Austin and Dallas. Here is the relevant data.

![Screen_Shot_2020-09-30_at_12.47.08_PM.png](Screen_Shot_2020-09-30_at_12.47.08_PM.png)

Total capital available for investment is $11M. You can’t build more than one factory (warehouse) in one place. At most one warehouse must be built in Austin or Dallas. At least one factory must be built in Austin or Dallas. Find the optimal investment strategy.

 

Is building the Factory in Dallas part of the optimal investment strategy?

## Question 3

Western Airlines wants to design a hub system in the United States. Each hub is used for connecting flights to and from cities within 1000 miles of the hub. Western runs flights among the following cities: Atlanta (ATL), Boston (BOS), Chicago (CHI), Denver (DEN), Houston (HOU), Los Angeles (LAX), New Orleans (NO), New York (NY), Pittsburgh (PIT), Salt Lake City (SLC), San Francisco (SF), and Seattle (SEA). The company wants to determine the smallest number of hubs it needs to cover all these cities, where a city is covered if it is within 1000 miles of at least one hub. The table below lists which cities are within 1000 miles of other cities. For example, if a hub was placed at Boston (BOS), it could cover the cities of Boston, New York, and Pittsburgh.

![Screen_Shot_2020-09-30_at_12.52.50_PM](Screen_Shot_2020-09-30_at_12.52.50_PM.png)

Formulate and solve this problem as a binary integer program.

 

Is SLC a hub in the optimal solution?


## Question 4

A paper mill cuts the rolls of paper into different widths to satisfy customers’ demand. In this problem, assume the original rolls of paper are 120 inches wide. The table below shows the orders received by the paper mill.

![Screen_Shot_2020-09-30_at_12.56.55_PM](Screen_Shot_2020-09-30_at_12.56.55_PM.png)

A 120 inch roll can be cut in many ways. For example, we can cut four 25-inch rolls while wasting the remaining 20 inches; we can also cut one 25-inch, one 37-inch, and one 54-inch. In the second case, only 4 inches is wasted.

Develop and solve an integer program to minimize the waste from cutting to satisfy all orders.  For more information, you can check out the cutting stock problem on wikipedia: https://en.wikipedia.org/wiki/Cutting_stock_problem (Links to an external site.)

 

How many rolls get cut into the pattern such that there are 3 cuts of 25 inches, and 1 cut of 37 inches (this pattern results in 8" waste)?



## Question 5

The days-off scheduling problem must be solved routinely by businesses that operate 6 or 7 days a week. Examples include hospitals, airlines, municipal transportation companies, and the postal service. The most common example is the (5,7)-cyclic staffing problem. The objective of it is to minimize the cost of assigning workers to a 7-day cyclic schedule so that

1) Sufficient workers are available every day.

2) Each person works 5 consecutive days and is idle to the remaining 2 days.

Here is the table showing the cost of having an employee for each day and the number of employees required for each day.

![Screen_Shot_2020-09-30_at_1.07.29_PM](Screen_Shot_2020-09-30_at_1.07.29_PM.png)

For example, the pattern that one works from Sunday to Thursday costs 90 + 60 × 4 = 330.

Formulate and solve an integer programming problem to represent this problem.

How many employees work Monday-Friday?
