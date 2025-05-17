# EX 5B Coin Change Problem
## DATE: 15/04/2025
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1. Initialize a table to store the minimum number of coins for each amount (0 to target).

2. Iterate through each amount and each coin denomination.

3. Calculate the minimum coins needed for the current amount using the current coin.

4. The last entry in the table gives the final result.
 

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: LAVANYA S
Register Number: 212223230112
*/
class Solution(object):
    def coinChange(self, coins, amount):
        dp=[float('inf')]*(amount+1)
        dp[0]=0
        for coin in coins:
            for i in range(coin,amount+1):
                dp[i]=min(dp[i],dp[i-coin]+1)
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

![image](https://github.com/user-attachments/assets/c6d3c55d-b6ef-4ad4-9eea-d720434bbb10)



## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
