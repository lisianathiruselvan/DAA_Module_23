# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm
1. Initialize max_till_now with the first element and max_ending as 0.

2. Iterate through the array, adding each element to max_ending.

3. If max_ending becomes negative, reset it to 0 (discard the current subarray).

4. If max_ending exceeds max_till_now, update max_till_now.

5. Return max_till_now as the maximum contiguous subarray sum.
  

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: LISIANA T
Register Number: 212222240053 
*/
def maxSubArraySum(a,size):
    
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output:

![image](https://github.com/user-attachments/assets/9c5b80a3-0a94-43cc-8adf-9a8e3468e033)


## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
