#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given an array of integers `a`, find the length of longest subarray where the absolute difference between any two elements is less than or equal to `1`. 
#### Sample Input :point_down:
```
a = [1, 2, 2, 3, 1, 2]
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
`[1, 2, 2, 1, 2]` is the longest subarray where the absolute difference between any two elements is less than or equal to `1`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    c = [0] * 100 # frequency count
    
    for i in a:
        c[i] += 1
        
    m = 0 # max subarray length
    for i in range(1, 100):
        m = max(m, c[i] + c[i-1]) 
            
    return m
```  
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/picking-numbers/problem)
