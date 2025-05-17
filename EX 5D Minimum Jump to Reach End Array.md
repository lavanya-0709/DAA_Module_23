# EX 5D Minimum Jump to Reach End Array
## DATE: 22/04/2025
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1.Create a jumps[] array of size n, initialized with infinity (inf), except jumps[0] = 0.

2.Loop through the array from index 1 to n-1.

3.For each i, check all previous indices j < i. If arr[j] + j >= i, update: jumps[i] = min(jumps[i], jumps[j] + 1)

4.Return jumps[n-1] as the minimum number of jumps to reach the end. 
 

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: LAVANYA S
Register Number: 212223230112
*/
def minJumps(arr, n):
    jumps=[0 for _ in range(n)]
    if (n==0 or arr[0]==0):
        return float('inf')
    jumps[0]=0
    for i in range(1,n):
        jumps[i]=float('inf')
        for j in range(i):
            if(i<=arr[j]+j) and (jumps[j]!=float('inf')):
                jumps[i]=min(jumps[i],jumps[j]+1)
                break
    return jumps[n-1]
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
 
```

## Output:

![image](https://github.com/user-attachments/assets/f659de05-efb3-4996-ac6f-01a3059ee649)



## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
