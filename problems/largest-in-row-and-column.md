#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-prefix--sum-wheat) 

#### Problem :point_down:
You are given a two-dimensional array of integers `m` containing `1`s and `0`s. Return the number of elements in matrix such that
- `m[r][c] = 1`
- `m[r][j] = 0` for every `j ≠ c` and `m[i][c] = 0` for every `i ≠ r`

#### Sample Input :point_down:
```
m = [
    [0, 0, 1],
    [1, 0, 0],
    [0, 1, 0]
]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
We have `m[0][2]`, `m[1][0]` and `m[2][1]` meet the criteria.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(self, m):
    r = [0 for i in range(len(m))]
    c = [0 for j in range(len(m[0]))]
    for i in range(len(m)):
        for j in range(len(m[i])):
            if m[i][j] == 1:
                r[i] += 1
                c[j] += 1

    n = 0
    for i in range(len(m)):
        for j in range(len(m[i])):
            if m[i][j] == 1 and (r[i] == 1 and c[j] == 1):
                n += 1

    return n
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

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Largest-Elements-in-Their-Row-and-Column)
