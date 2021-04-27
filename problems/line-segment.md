#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an array of `[x, y]` coordinates `c` in a Cartesian plane, return whether the coordinates form a straight line segment.
#### Sample Input :point_down:
```
c = [
    [1, 1],
    [3, 3],
    [7, 7]
]
```
#### Sample Output :point_down:
```
True
```
#### Explanation :point_down:
<img src="https://raw.githubusercontent.com/er-knight/coding-problems/main/assets/line-segment.png" width="200">

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(c):
    (x0, y0), (x1, y1) = c[0], c[1]
    for i in range(2, len(c)):
        x, y = c[i]
        if ((x0 - x1) * (y1 - y)) != ((x1 - x) * (y0 - y1)):
            return False

    return True
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
[binarysearch.com](https://binarysearch.com/problems/Line-Segment)
