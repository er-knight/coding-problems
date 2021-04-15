#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-prefix--sum-wheat) 

#### Problem :point_down:
Given a two-dimensional integer matrix `m`, return a new matrix `a` of the same dimensions where each element is set to  
`a[i][j] = sum(m[r][c])` for all `r ≤ i`, `c ≤ j`.
#### Sample Input :point_down:
```
m = [
    [2, 3],
    [5, 7]
]
```
#### Sample Output :point_down:
```
[
    [2, 5],
    [7, 17]
]
```
#### Explanation :point_down:
sum along rows:
- `m[0][1] = m[0][0] + m[0][1] = 2 + 3 = 5`
- `m[1][1] = m[0][1] + m[1][1] = 5 + 7 = 12`

sum along columns:
- `m[1][0] = m[0][0] + m[1][0] = 2 + 5 = 7`
- `m[1][1] = m[0][1] + m[1][1] = 5 + 12 = 17`
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(m):
    for i in range(len(m)):
        for j in range(1, len(m[i])):
            m[i][j] += m[i][j-1]

    for i in range(1, len(m)):
        for j in range(len(m[0])):
            m[i][j] += m[i-1][j]

    return m
```  
#### Time Complexity :point_down:
```
O(r * c)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Matrix-Prefix-Sum)
