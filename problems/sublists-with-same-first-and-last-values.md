#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an array of integers `a`, return the number of sublists where the first element and the last element have the same value.
#### Sample Input :point_down:
```
a = [1, 5, 3, 1]
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
The sublists with same first and last element are: `[1], [5], [3], [1], [1, 5, 3, 1]`.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    c = 0
    for i in d.values():
        c += (i * (i + 1)) // 2

    return c
```  
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
o(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Count-of-Sublists-with-Same-First-and-Last-Values)
