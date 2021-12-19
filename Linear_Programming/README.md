## Question 1

Max is in a pie eating contest that lasts 1 hour. Each torte that he eats takes 2 minutes to eat. Each apple pie that he eats takes 3 minutes. He receives 4 points for each torte and 5 points for each pie. Find the number of tortes and apple pies Max should eat to get the most points. Solve the problem using the graphical method.

Next, let’s see what happens if he would like to stick to his preference of eating at least as many pies as tortes. That is; the number of pies he eats should be greater than or equal to the number of tortes.

 

By how many points does this constraint decrease Max’s total points? (this is the part you will submit to the canvas answer.)


## Question 2

A farmer in Iowa owns 450 acres of land. He is going to plant each acre with wheat or corn. Each acre planted with wheat (corn) yields $2,000 ($3,000) profit, requires three (two) workers, and requires two (four) tons of fertilizer. There are currently 1,000 workers and 1,200 tons of fertilizer available.

 

Formulate and solve this problem using gurobi.

 

Next we want to see What happens to the decision variables and the total profit when the availability of fertilizer varies from 200 tons to 2200 tons in 100-ton increments.

 

At what level of fertilizer does the farmer discontinue producing wheat?  That is, what is the smallest level of available fertilizer that results in no wheat being produced?  Your answer should be one of the 100 ton incremental numbers, like 600 or 1300 or...

## Question 3

Star Oil Company is considering five different investment opportunities. The table below gives the required cash outflows and net present values in millions of dollars.

Star Oil has $40 million available for investment now (time 0); it estimates that one year from now (time 1) $20 million will be available for investment. Star Oil may purchase any fraction of each investment, but no more than 100% of each opportunity. In this case, the cash outflows and NPV are adjusted accordingly.

For example, if Star Oil purchases one-fifth of investment 3, then a cash outflow of 1/5 × 5 = 1 million dollars would be required at time 0, and a cash outflow of 1/5 × 5 = 1 million would be required at time 1. The one-fifth share of investment three would yield an NPV of 1/5 ∗ 16 = 3.2 million dollars. Star Oil wants to maximize the NPV that can be obtained by investing in investments 1-5. Formulate an LP that will help achieve this goal. Assume that any funds leftover at time 0 cannot be used at time 1.

What percentage of opportunity 3 should be Star Oil invest in?  Answer in decimals, so if your answer is 54%, you should input 0.54.  Round 2 to decimal places

![Screen_Shot_2020-09-14_at_1.19.51_PM](Screen_Shot_2020-09-14_at_1.19.51_PM.png)



## Question 4

The goal of this problem is to select a set of foods that will satisfy a set of daily nutritional requirement at minimum cost. Suppose there are three foods available, corn, milk, and bread. There are restrictions on the number of calories (between 2000 and 2250) and the amount of Vitamin A (between 5000 and 50,000) that can be eaten. The table below shows, for each food, the cost per serving, the amount of Vitamin A per serving, and the number of calories per serving. Also, the maximum number of servings for each food is 10.

How many servings of corn should you eat?  Round to 2 decimal places.

![Screen_Shot_2020-09-14_at_1.24.01_PM](Screen_Shot_2020-09-14_at_1.24.01_PM.png)

## Question 5

Paper and wood products companies need to define cutting schedules that will maximize the total wood yield of their forests over some planning period. Suppose that a firm with control of 2 forest units wants to identify the best cutting schedule over a planning horizon of 3 years. Forest unit 1 has a total acreage of 2 and unit 2 has a total of 3 acres. The studies that the company has undertaken predict that each acre in unit 1(2) will have 1, 1.3, 1.4 (1, 1.2, 1.6) tons of woods per acre available for harvesting in year 1, 2, 3 respectively. Based on its prediction of economic conditions, the company believes that it should harvest at least 1.2, 1.5, 2 tons of wood in year 1, 2, 3 separately. Due to the availability of equipment and personnel, the company can harvest at most 2, 2, 3 tons of wood in year 1, 2, 3. Find the company’s best cutting strategy that maximizes the total weights of wood. Here discounting of the time value should not be considered.  If some fraction of a forest unit is cut down in year 1, that part of the forest cannot be cut again for the remaining 2 years.  Similarly if some fraction of the forest unit is cut down in year 2 it cannot be cut in year 3.

 

In year 3, how many acres of forest unit 2 should be cut down?  Round to 2 decimal places.
