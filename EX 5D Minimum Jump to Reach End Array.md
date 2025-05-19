# EX 5D Minimum Jump to Reach End Array
## DATE: 26.4.25
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. Initialize a jumps array to store the minimum jumps needed to reach each index.

2. Set jumps[0] = 0; all other values start as inf (unreachable initially).

3. Iterate through each index i from 1 to n-1.

4. For each i, check previous indices j to see if i is reachable from j, and update jumps[i].

5. Return jumps[n-1], which gives the minimum jumps to reach the end of the array.

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: LISIANA T
Register Number: 212222240053 
*/
def minJumps(arr, n):
    ##########  Add your code here ##############
    jumps = [0 for i in range(n)]
 
    if (n == 0) or (arr[0] == 0):
        return float('inf')
 
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
 
```

## Output:

![image](https://github.com/user-attachments/assets/cdc148ff-b374-4fe7-8ac6-f2bdb3d55fc5)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
