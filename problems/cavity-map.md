#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given a square map `m` as a matrix of integer strings. Each cell of the map has a value denoting its depth. We will call a cell of the map a cavity if and only if this cell is not on the border of the map and each cell adjacent to it has strictly smaller depth. Two cells are adjacent if they have a common side, or edge.

Find all the cavities on the map and replace their depths with the uppercase character `X`. 
#### Sample Input :point_down:
```
m = [
    '1112', 
    '1912', 
    '1892', 
    '1234'
]
```
#### Sample Output :point_down:
```
[
    '1112', 
    '1X12', 
    '18X2', 
    '1234'
]
```
#### Explanation :point_down:
The two cells with the depth of `9` are not on the border and are surrounded on all sides by shallower cells. Their values are replaced by `X`. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    c = [] # cavities
    for i in range(1, len(m)-1):
        for j in range(1, len(m[i])-1):
            e = [m[i-1][j], m[i+1][j], m[i][j-1], m[i][j+1]] # edges
            if all([m[i][j] > k for k in e]):
                c.append([i, j])
    
    for i, j in c:
        m[i] = m[i][:j] + 'X' + m[i][j+1:]
        
    return m
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/cavity-map/problem)
