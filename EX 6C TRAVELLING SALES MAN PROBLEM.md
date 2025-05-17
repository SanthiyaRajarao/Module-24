# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE: 09/05/25
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm

1. List all vertices except the start vertex.
2. Generate all permutations of these vertices.
3. Calculate the total path length for each permutation including return to start.
4. Track and update the minimum path length found.
5. Return the minimum path length as the shortest route.


## Program:
```
/*
To implement the program for TSP.


Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
    vertex = [] 
    for i in range(V): 
        if i != s: 
            vertex.append(i) 
    min_path = maxsize 
    next_permutation=permutations(vertex)
    for i in next_permutation:

        current_pathweight = 0
        k = s 
        for j in i: 
            current_pathweight += graph[k][j] 
            k = j 
        current_pathweight += graph[k][s] 
        min_path = min(min_path, current_pathweight) 
         
    return min_path
   

if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))

```

## Output:

![image](https://github.com/user-attachments/assets/a465e1a4-41ba-4526-9387-926d84a6a17c)


## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
