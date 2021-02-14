#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given an `m x n` matrix, return `true` if the matrix is Toeplitz. Otherwise, return `false`.  
A matrix is Toeplitz if every diagonal from top-left to bottom-right has the same elements.
#### Sample Input :point_down:
```
m = [
    [1,2,3,4],
    [5,1,2,3],
    [9,5,1,2]
] 
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
In the above grid, the diagonals are:
```
[9], [5, 5], [1, 1, 1], [2, 2, 2], [3, 3], [4].
```
In each diagonal all elements are the same, so the answer is `true`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    for i in range(1, len(m)):
        for j in range(1, len(m[i])):
            if (m[i][j] != m[i-1][j-1]):
                return False

    return True
```
#### Time Complexity :point_down:
```
O(m * n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/toeplitz-matrix/)  
[binarysearch.com](https://binarysearch.com/problems/Toeplitz-Matrix)
