# EX 5C Kadane's Algorithm
## DATE: 19/04/2025
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm
1.Initialize:

a.max_so_far = 0 (stores the overall maximum sum)

b.current_max = 0 (stores the maximum sum ending at the current position)

2.Iterate: Loop through the array elements.

3.Update current_max: For each element, add it to current_max.

4.Update max_so_far and Reset current_max:

a.If current_max > max_so_far, update max_so_far to current_max.

b.If current_max < 0, reset current_max to 0. 

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: LAVANYA S
Register Number: 212223230112
*/
def maxSubArraySum(a,size):
    m=a[0]
    for i in range(1,size):
        a[i]=max(a[i],a[i]+a[i-1])
        m=max(m,a[i])
    return m
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output:

![image](https://github.com/user-attachments/assets/3331c971-3827-43a2-910b-e5ea10ce4d1d)



## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
