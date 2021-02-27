#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-binary--search-wheat)

#### Problem :point_down:
Given an array of unique integers `a` sorted in ascending order, return the minimum `i` such that `nums[i] == i`. If there's no solution, return `-1`.
#### Sample Input :point_down:
```
a = [-5, -2, 0, 3, 4]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
Both `nums[3] == 3` and `nums[4] == 4` but `3` is smaller.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    for i in range(len(a)):
        if a[i] == i:
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
#### [@xiaowuc1](https://binarysearch.com/problems/Fixed-Point/editorials/3517068)'s Python Solution :point_down:
```py
def solve(a):
    k = -1
    i = 0
    j = len(a) - 1

    while i <= j:
        m = (i + j)//2
        if a[m] == m:
            k = m
        if a[m] >= m:
            j = m - 1
        else:
            i = m + 1

    return k
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Fixed-Point)
