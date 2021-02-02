#### Topics :point_down:
![](https://img.shields.io/badge/-matrix-wheat)

#### Problem :point_down:
Given a matrix of integers of size `n x n`, find the maximum sum of integers in any sub-matrix of size `k x k`.  
Note: Integers may be negative.
#### Sample Input :point_down:
```
n = 5
k = 3
matrix = [
    [1, 1, 1, 1, 1],
    [2, 2, 2, 2, 2],
    [3, 8, 6, 7, 3],
    [4, 4, 4, 4, 4],
    [5, 5, 5, 5, 5]
]
```
#### Sample Output :point_down:
```
48
```
#### Explanation :point_down:
```
[[8, 6, 7],
 [4, 4, 4],
 [5, 5, 5]]
```
Above sub-matrix has maximum sum = `48`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(matrix, n, k):
    max_sum = 0
    temp_sum = 0
    for i in range(n-k+1):
        for j in range(n-k+1):
            for l in range(k):
                for m in range(k):
                    temp_sum += matrix[i+l][j+m]
            max_sum = max(max_sum, temp_sum)
            temp_sum = 0
            
    return max_sum
```
#### Time Complexity :point_down:
```
O(n^2 * k^2) 
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(matrix, n, k):
    strip_sum = [[0 for i in range(n)] for j in range(n)]
        
    for j in range(n):
        temp_sum = 0
        
        for i in range(k):
            temp_sum += matrix[i][j]
        strip_sum[0][j] = temp_sum
        
        for i in range(1, n-k+1):
            temp_sum += (matrix[i+k-1][j] - matrix[i-1][j])
            strip_sum[i][j] = temp_sum
    
    max_sum = -math.inf
    
    for i in range(n-k+1):
        temp_sum = 0
        for j in range(k):
            temp_sum += strip_sum[i][j]
            
        max_sum = max(max_sum, temp_sum)
        
        for j in range(1, n-k+1):
            temp_sum += (strip_sum[i][j+k-1] - strip_sum[i][j-1])
            max_sum = max(max_sum, temp_sum)
            
    return max_sum
```
#### Time Complexity :point_down:
```
O(n^2)
```
#### Space Complexity :point_down:
```
O(n^2)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/print-maximum-sum-square-sub-matrix-of-given-size/)
