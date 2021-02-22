#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given an `n` by `n` integer matrix `m`, return the sum of all elements that form a Z in the matrix.
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
35
```
#### Explanation :point_down:
The Z that's formed is `[1, 2, 3, 5, 7, 8, 9]` and its sum is `35`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    n = len(m)

    if n == 1:
        return m[0][0]

    s = sum(m[0]) + sum(m[-1])

    i = 1
    j = n-2
    while (i < n-1 and j > 0):
        s += m[i][j]
        i += 1
        j -= 1

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
[binarysearch.com](https://binarysearch.com/problems/Z-Sum)
