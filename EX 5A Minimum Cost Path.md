# EX 5A Minimum Cost Path
## DATE: 12/04/2025
## AIM: 
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.




## Algorithm
1.Base Cases: Reach destination: return cell cost. Go out of bounds: return infinity.

2.Recursive Calls: Explore down, right, and diagonal paths.

3.Calculate Cost: Add current cell cost to the minimum cost of the explored paths.

4.Return: The minimum cost to reach the destination. 
   

## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: LAVANYA S
Register Number: 212223230112
*/
R = int(input())
C = int(input())
import sys
def minCost(cost, m, n):
    if (n<0 or m<0):
        return sys.maxsize
    elif (m==0 and n==0):
        return cost[m][n]
    else:
        return cost[m][n]+min(minCost(cost,m-1,n-1),minCost(cost,m-1,n),minCost(cost,m,n-1))
    ###########  Add your Code Here ##################
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

![image](https://github.com/user-attachments/assets/9b40aef1-3b61-4881-9e0e-16894a5a4f37)


## Result:
Thus the above program was executed successfully for finding the minimum cost.
