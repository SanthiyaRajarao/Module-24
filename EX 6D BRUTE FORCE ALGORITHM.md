# EX 6D BRUTE FORCE ALGORITHM
## DATE: 13/05/25
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.




## Algorithm

1. Calculate lengths of the main string and substring
2. Loop through the main string up to the point where substring can fit
3. Extract substring-length slices from the main string
4. Compare each slice with the target substring
5. Print the starting index whenever a match is found


## Program:
```
/*
To implement the program using brute force method of searching for the given substring in the main string.


Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
def match(string,sub):
    l = len(string)
    ls = len(sub)
    start = sub[0]
    for i in range(l-ls+1):
        if string[i:i+ls]==sub:
            print(f"Found at index {i}")

str1=input()
str2=input()
```

## Output:

![image](https://github.com/user-attachments/assets/22fa4df2-379a-40f0-b364-5d3540ac4a81)


## Result:
Thus the above program was executed successfully for searching the substring at respective index.
