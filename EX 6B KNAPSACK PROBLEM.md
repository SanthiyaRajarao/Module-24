# EX 6B KNAPSACK PROBLEM
## DATE: 06/05/25
## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.



## Algorithm

1. Initialize a 2D Table for Dynamic Programming
2. Set Base Conditions for Zero Items or Zero Capacity
3. Iterate Over Each Item and Each Capacity Value
4. Check if Current Item Can Fit in the Current Capacity
5. Decide Whether to Include or Exclude the Current Item
6. Call the Knapsack Function and Display the Result

## Program:
```
/*
To implement the program for 0/1 knapsack problem.


Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
def knapSack(W, wt, val, n):
    K = [[0 for x in range(W + 1)] for x in range(n + 1)]
    for i in range(n + 1):
        for w in range(W + 1):
            if i == 0 or w == 0:
                K[i][w] = 0
            elif wt[i-1] <= w:
                K[i][w] = max(val[i-1]+ K[i-1][w-wt[i-1]],K[i-1][w])
            else:
                K[i][w] = K[i-1][w]
 
    return K[n][W]

x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))

n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
```

## Output:



![image](https://github.com/user-attachments/assets/f95601ff-f68a-4dcc-bc04-418c9d95e02f)

## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
