#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given an array of coordinates `c`, `c[i] = [x, y]`, where `[x, y]` represents the coordinate of a point. Check if these points make a straight line in the XY plane.
#### Sample Input :point_down:
```
c = [[1, 2], [2, 3], [3, 4], [4, 5], [5, 6], [6, 7]]
````
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
<img src="https://assets.leetcode.com/uploads/2019/10/15/untitled-diagram-2.jpg" width="250">
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c):
    if len(c) == 2:
        return True

    x1, y1, x2, y2 = c[0][0], c[0][1], c[1][0], c[1][1]

    for i in range(1, len(c)):
        x3, y3 = c[i][0], c[i][1]
        if not((y3 - y2) * (x2 - x1) == (y2 - y1) * (x3 - x2)):
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/program-check-three-points-collinear/)

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/check-if-it-is-a-straight-line/)
