### A transportation cost problem - minimizing the cost of transportation

This analysis is an answer to the question 26 case problem of the first chapter of the book "Introduction to Management Science" from the author Bernard W. Taylor. 

#### 📜Case description:
The Easy Drive Car Rental Agency needs 500 new cars in its Nashville operation and 300 new cars in Jacksonville, 
and it currently has 400 new cars in both Atlanta and Birmingham. It costs $30 to move a car from Atlanta to Nashville, 
$70 to move a car from Atlanta to Jacksonville, $40 to move a car from Birmingham to Nashville, 
and $60 to move a car from Birmingham to Jacksonville. 
The agency wants to determine how many cars should be transported from the agencies in Atlanta and Birmingham to the agencies in Nashville and Jacksonville
in order to meet demand while minimizing the transport costs. Develop a mathematical model for this problem and use logic to determine a solution.

#### 📜Answers:
Two methods were used to find the answer:
- Method one: In this method, a manual approach was used to find the scenario of transportation that returns the lowest total cost for the combination of each route. No optimization packages were used.
- Method two: In this method, PuLP, a optimization package, was used. It saves time of resolution and reduces the time spent writhing code.

---
The problem can be modelled considering each possible route as a variable and implementing constraints based on the capacity of each agency.

##### Possible routes with respective prices and variables
Atlanta to Nashville: \\$30 per car, x cars
<br>
Atlanta to Jacksonville: \\$70 per car, y cars
<br>
Birmingham to Nashville: \\$40 per car, w cars
<br>
Birmingham to Jacksonville: \\$60 per car, z cars

##### The cost to be minimized is the sum of the product of each price and each the number of cars moved from a agency to another.
Minimize C = 30*x + 70*y + 40*w + 60*z
<br>
##### And the possible scenarios of cost is restricted by the total number of cars that can be moved from a agency to another:
Subject to:
<br>
x + y = 400
<br>
w + z = 400
<br>
x + w = 500
<br>
y + z = 300

Both methods return the same answer: 

The lowest cost, $34000.0, is achieved when 
400 cars are moved from Atlanta to Nashville, 
0 cars are moved from Atlanta to Jacksonville, 
100 cars are moved from Birmingham to Nashville and 
300 cars are moved from Birmingham to Jacksonville
