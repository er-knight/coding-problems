#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) ![](https://img.shields.io/badge/-prefix--sum-wheat)

#### Problem :point_down:
Given an array `a` of `n` positive numbers, find the first equilibium-point in the array. 
Equilibrium point in an array is a index such that the sum of elements before it is equal to the sum of elements after it.

#### Sample Input :point_down:
```
n = 5
a = [1, 3, 5, 2, 2]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Equilibrium point is at index `2` (0-based) as sum of elements before it `1 + 3 = 4` is equal to sum of elements after it `2 + 2 = 4`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, n):
    prefix_sum = []
    suffix_sum = []
    
    sum_ = 0
    for i in range(n):
      sum_ += a[i]
      prefix_sum.append(sum_)
    
    sum_ = 0
    a_sum = sum(a)
    for i in range(n):
      suffix_sum.append(a_sum - sum_)
      sum_ += a[i]
    
    for i in range(n):
      if prefix_sum[i] == suffix_sum[i]:
        return i
        
    return -1
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```

#### Python :point_down:
```py
def solve(a, n):
    right_sum = sum(a) - a[0]
    left_sum = 0
    
    if (left_sum == right_sum):
        return 0
    
    for i in range(1, n):
        left_sum += a[i-1]
        right_sum -= a[i]

        if (left_sum == right_sum):
            return i
    
    return -1
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/find-element-array-sum-left-array-equal-sum-right-array/)

#### Solve Here :point_down:
[geeksforgeeks.org](https://practice.geeksforgeeks.org/problems/equilibrium-point-1587115620/1)  
[binarysearch.com](https://binarysearch.com/problems/Index-with-Equal-Left-and-Right-Sums)  
[leetcode.com](https://leetcode.com/problems/find-pivot-index/)
