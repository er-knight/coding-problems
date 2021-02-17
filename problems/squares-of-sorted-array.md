#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an integer array `a` sorted in non-decreasing order, return an array of the squares of each number sorted in non-decreasing order.
#### Sample Input :point_down:
```
a = [-4, -1, 0, 3, 10]
```
#### Sample Output :point_down:
```
[0, 1, 9, 16, 100]
```
#### Explanation :point_down:
After squaring, the array becomes `[16, 1, 0, 9, 100]`.
After sorting, it becomes `[0, 1, 9, 16, 100]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    o = [0 for i in a] # output 

    l = 0        # left
    r = len(a)-1 # right
    for i in range(r, -1, -1):
        if abs(a[l]) >= abs(a[r]):
            o[i] = a[l] ** 2
            l += 1
        else:
            o[i] = a[r] ** 2
            r -= 1

    return o
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
[leetcode.com](https://leetcode.com/problems/squares-of-a-sorted-array/)
