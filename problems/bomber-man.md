
#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)

#### Problem :point_down:
You are given a two-dimensional integer matrix `m` of `1`s and `0`s, where a `1` represents a bomb and `0` represents an empty cell. When a bomb explodes, all the spaces along on the same row and column are damaged. Return the number of spaces you can stand in to not get damaged.
#### Sample Input :point_down:
```
m = [
    [1, 0, 0],
    [0, 1, 0],
    [0, 0, 0]
]
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
Represent all damaged spaces by `1`
```
m = [
    [1, 1, 1],
    [1, 1, 1],
    [1, 1, 0]
]
```
`m[2][2]` is only safe space. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    r = {} # unsafe rows
    c = {} # unsafe columns
    for i in range(len(m)):
        for j in range(len(m[i])):
            if m[i][j]:
                r[i] = False
                c[j] = False

    s = 0 # safe spaces
    for i in range(len(m)):
        for j in range(len(m[i])):
            if r.get(i, True) and c.get(j, True):
                s += 1

    return s
```  
#### Python :point_down:
```py
def solve(m):
    r = set() # unsafe rows
    c = set() # unsafe columns
    for i in range(len(m)):
        for j in range(len(m[i])):
            if m[i][j]:
                r.add(i)
                c.add(j)

    s = 0 # safe spaces
    for i in range(len(m)):
        for j in range(len(m[i])):
            if (i not in r) and (j not in c):
                s += 1

    return s
```  
#### Explanation :point_down:
If `m[i][j] = 1`, then add `ith` row and `jth` column, because all spaces in `ith` row and `jth` column are going to explode.
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
[binarysearch.com](https://binarysearch.com/problems/Bomber-Man)
