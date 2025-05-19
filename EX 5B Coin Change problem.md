# EX 5B Coin Change Problem
## DATE:
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1. Initialize a DP array of size amount + 1 with inf, and set dp[0] = 0 (0 coins needed for amount 0).

2. Iterate over each coin in the given list.

3. For each coin, update the dp array from index coin to amount.

4. At each step, set dp[i] = min(dp[i], dp[i - coin] + 1) to track the fewest coins needed.

5. Return dp[amount] if it's not inf; otherwise, return -1 (not possible).

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: LISIANA T
Register Number: 212222240053 
*/
class Solution(object):
   def coinChange(self, coins, amount):
     
       dp = [float('inf')] * (amount + 1)
       dp[0]=0
       for coin in coins:
           for i in range(coin, amount + 1):
               dp[i] = min(dp[i], dp[i - coin] + 1)
       return dp[amount] if dp[amount]!=float('inf') else -1
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```

## Output:

![image](https://github.com/user-attachments/assets/9087f94e-3ee2-4d7c-ac8d-602e0fa27878)


## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
