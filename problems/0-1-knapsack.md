#### Topics :point_down:
![](https://img.shields.io/badge/-dynamic--programming-wheat) 

#### Problem :point_down:
You are given two integer arrays `w` (weights) and `v` (values) which have the same length and an integer capacity. `w[i]` and `v[i]` represent the weight and value of the `ith` item.  
Given that you can take at most `c` (capacity) weights, and that you can only take at most one copy of each item, return the maximum amount of value you can get.
#### Sample Input :point_down:
```
w = [1, 2, 3]
v = [1, 5, 3]
c = 5
```
#### Sample Output :point_down:
```
8
```
#### Explanation :point_down:
Take `w[1] = 2` and `w[2] = 3`.
```
v[1] + v[2] = 5 + 3 = 8
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(w, v, c):
    n = len(w)
    k = [[0 for i in range(c+1)] for j in range(n+1)] # knapsack
    for i in range(n+1):
        for j in range(c+1):
            if i == 0 or j == 0:
                k[i][j] = 0
            elif w[i-1] <= j:
                k[i][j] = max(v[i-1] + k[i-1][j-w[i-1]], k[i-1][j])
            else:
                k[i][j] = k[i-1][j]

    return k[n][c]
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/0-1-knapsack-problem-dp-10/)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/0-1-Knapsack)
