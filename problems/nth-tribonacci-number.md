#### Topics :point_down:
![](https://img.shields.io/badge/-dynamic--programming-wheat) 
![](https://img.shields.io/badge/-recursion-wheat)

#### Problem :point_down:
The Tribonacci sequence `T` is defined as follows: 
```
T[0] = 0 
T[1] = 1 
T[2] = 1
T[n] = T[n-1] + T[n-2] + T[n-3] for n > 3.
```
Given `n`, return the value of `T[n]`.
#### Sample Input :point_down:
```
n = 4
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
```
T[3] = T[2] + T[1] + T[0] = 1 + 1 + 0 = 2
T[4] = T[3] + T[2] + t[1] = 2 + 1 + 1 = 4
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    t = [0, 1, 1]
    for i in range(3, n+1):
        t.append(t[i-1] + t[i-2] + t[i-3])
    return t[n]
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```   
#### Python :point_down:
```py
def solve(n):
    if (n == 0):
        return n
    a, b, c = 0, 1, 1
    for i in range(3, n+1):
        a, b, c = b, c, (a + b + c)
    return c
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
[leetcode.com](https://leetcode.com/problems/n-th-tribonacci-number/)
