# EX 5A Minimum Cost Path
## DATE: 14.4.25
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.




## Algorithm
1. Base Case: If either index is negative, return infinity (invalid path).

2. If at the starting cell (0,0), return its cost directly.

3. Recursively compute the minimum cost to reach the current cell from the left, top, and diagonal cells.

4. Add current cell’s cost to the minimum of the three recursive paths.

5. Return the total cost, which represents the minimum cost to reach cell (m, n) from (0, 0).

## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: LISIANA T
Register Number: 212222240053 
*/
R = int(input())
C = int(input())
import sys
def minCost(cost, m, n):
    
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```

## Output:

![image](https://github.com/user-attachments/assets/a359cc3e-3ee4-4020-8356-6b76a47ec556)


## Result:
Thus the above program was executed successfully for finding the minimum cost.
