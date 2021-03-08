#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array `a`, rotate the array to the right by `k` steps, where `k` is non-negative.  
Follow up:
- Try to come up as many solutions as you can, there are at least 3 different ways to solve this problem.
- Could you do it in-place with `O(1)` extra space?

#### Sample Input :point_down:
```
a = [1, 2, 3, 4, 5, 6, 7]
k = 3
```
#### Sample Output :point_down:
```
[5, 6, 7, 1, 2, 3, 4]
```
#### Explanation :point_down:
```
rotate 1 steps to the right: [7, 1, 2, 3, 4, 5, 6]
rotate 2 steps to the right: [6, 7, 1, 2, 3, 4, 5]
rotate 3 steps to the right: [5, 6, 7, 1, 2, 3, 4]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, k):
    k = k % len(a)

    # reverse a[0:len(a)]
    i, j = 0, len(a)-1        
    while i < j:
        a[i], a[j] = a[j], a[i]
        i += 1
        j -= 1

    # reverse a[0:k]
    i, j = 0, k-1        
    while i < j:
        a[i], a[j] = a[j], a[i]
        i += 1
        j -= 1

    # reverse a[k:len(a)]
    i, j = k, len(a)-1        
    while i < j:
        a[i], a[j] = a[j], a[i]
        i += 1
        j -= 1
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

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/rotate-array/)
