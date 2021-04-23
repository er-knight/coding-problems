#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a clock time with hour `h` and integer minutes `m`, determine the smaller angle between the hour and the minute hands and floor it to the nearest integer.
#### Sample Input :point_down:
```
h = 12
m = 22
```
#### Sample Output :point_down:
```
121
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(h, m):
    a = abs((h * 30 + m * 0.5) - (m * 6)) % 360
    return min(floor(360 - a), floor(a))
```  
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Clock-Angle)
