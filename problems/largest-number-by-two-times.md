#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of integers `a`, return whether the largest number is bigger than the second-largest number by more than two times.
#### Sample Input :point_down:
```
a = [3, 6, 15]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`15` is bigger than `12 (2 * 6)`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    a.sort()
    return a[-1] > (a[-2] * 2)
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    m, n = -math.inf, -math.inf

    for i in a:
        if i >= m:
            m, n = i, m
        elif i > n:
            n = i

    return m > (2 * n)   
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
[binarysearch.com](https://binarysearch.com/problems/Largest-Number-By-Two-Times)
