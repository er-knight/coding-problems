#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a string `s` representing a number in base `3` (consisting only of `0`, `1`, or `2`), return its decimal integer equivalent. This should be implemented directly without using a built-in function.
#### Sample Input :point_down:
```
s = "21"
```
#### Sample Output :point_down:
```
7
```
#### Explanation :point_down:
```
7 = 2 * 3¹ + 1 * 3⁰
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s):
    d = 0 # decimal
    n = len(s)
    for i in range(n):
        d = d + int(s[n-i-1]) * (3 ** i)

    return d   
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(self, s):
    d = 0 # decimal
    for i in s:
        d = d * 3 + int(i)

    return d   
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(self, s):
    return int(s, base=3)    
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Base-3-to-Integer)
