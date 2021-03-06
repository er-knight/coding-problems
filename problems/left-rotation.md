#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
A left rotation operation on an array of size `n` shifts each of the array's elements unit to the left.  
Given an array `a` and an integer `d`, left rotate `a` `d` times and return the result. 
#### Sample Input :point_down:
```
a = [1, 2, 3, 4, 5]
d = 4
```
#### Sample Output :point_down:
```
[5, 1, 2, 3, 4]
```
#### Explanation :point_down:
To perform `d = 4` left rotations, the array undergoes the following sequence of changes:
```
[1, 2, 3, 4, 5] → [2, 3, 4, 5, 1] → [3, 4, 5, 1, 2] → [4, 5, 1, 2, 3] → [5, 1, 2, 3, 4]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, d):
    while d:
        for i in range(1, len(a)):
            a[i], a[i-1] = a[i-1], a[i]
            
        d -= 1
            
    return a
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(d, a):
    n = len(a)
    b = [0 for i in range(n)]   
    k = n - d

    for i in range(k):
        b[i] = a[d+i]  
    for i in range(k, n):
        b[i] = a[i-k]

    return b
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

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/array-left-rotation/problem)
