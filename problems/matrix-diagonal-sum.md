#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given a square matrix `m`, return the sum of the matrix diagonals.
Only include the sum of all the elements on the primary diagonal and all the elements on the secondary diagonal that are not part of the primary diagonal.
#### Sample Input :point_down:
```
m = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```
#### Sample Output :point_down:
```
25
```
#### Explanation :point_down:
<img src="https://assets.leetcode.com/uploads/2020/08/14/sample_1911.png" width="300">

```
Diagonals sum: 1 + 5 + 9 + 3 + 7 = 25
```
Notice that element `m[1][1] = 5` is counted only once.  
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    s = 0
    r, c = len(m), len(m)
    for i in range(r):
        for j in range(c):
            if (i != j) and (i+j == r-1):
                s += m[i][j]
            elif i == j:
                s += m[i][j]

    return s
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(m):
    s = 0
    n = len(m)
    for i in range(n):
        s += m[i][i]
        s += m[n-i-1][i]

    if n & 1:
        s -= m[n//2][n//2]

    return s
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
[leetcode.com](https://leetcode.com/problems/matrix-diagonal-sum/)
