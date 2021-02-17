#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given a 2D integer matrix `m`, return the transpose of matrix.  
The transpose of a matrix is the matrix flipped over its main diagonal, switching the matrix's row and column indices.
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
[
    [1, 4, 7],
    [2, 5, 8],
    [3, 6, 9]
]
```
#### Explanation :point_down:
<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/transpose.png" width="250">

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    r = len(m)    # rows
    c = len(m[0]) # columns
    t = [[0 for j in range(r)] for i in range(c)] # transpose
    for i in range(r):
        for j in range(c):
            t[j][i] = m[i][j]

    return t
```
#### Time Complexity :point_down:
```
O(r * c)
```
#### Space Complexity :point_down:
```
O(c * r)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/transpose-matrix/)
