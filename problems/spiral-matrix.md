#### Topics :point_down:
![](https://img.shields.io/badge/-matrix-wheat)

#### Problem :point_down:
Given a `matrix` of size `r x c`, print the matrix in spiral form.
#### Sample Input :point_down:
```
r = 3 
c = 3
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```
#### Sample Output :point_down:
```
1 2 3 6 9 8 7 4 5
```
#### Explanation :point_down:
<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/spiral-matrix-traversal.png" height="100">

#### Hint :point_down:
<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/spiral-matrix.png" height="220">
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(matrix, r, c):
    spiral = []
    q = 0 # rows
    b = 0 # columns
    while (q < r and b < c):
        for i in range(b, c):
            spiral.append(matrix[q][i])
        q += 1
 
        for i in range(q, r):
            spiral.append(matrix[i][c-1])
        c -= 1
 
        if (q < r):
            for i in range(c-1, b-1, -1):
                spiral.append(matrix[r-1][i])
            r -= 1
 
        if (b < c):
            for i in range(r-1, q-1, -1):
                spiral.append(matrix[i][b])
            b += 1
 
    return spiral
```
#### Time Complexity :point_down:
```
O(r * c)
```
#### Space Complexity :point_down:
```
O(r + c)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/print-a-given-matrix-in-spiral-form/)
#### Solve Here :point_down:
[geeksforgeeks.org](https://practice.geeksforgeeks.org/problems/spirally-traversing-a-matrix-1587115621/1)
