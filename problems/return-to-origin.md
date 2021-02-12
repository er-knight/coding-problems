#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
There is a robot starting at position `(0, 0)`, the origin, on a 2D plane. Given a sequence of its moves `m`, judge if this robot ends up at  
`(0, 0)` after it completes its moves.  
The move sequence is represented by a string, and the character `m[i]` represents its ith move. Valid moves are `R` (right), `L` (left), `U` (up), and `D` (down). If the robot returns to the origin after it finishes all of its moves, return `true`. Otherwise, return `false`.
#### Sample Input :point_down:
```
m = "UD"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
The robot moves up once, and then down once. All moves have the same magnitude, so it ended up at the origin where it started. Therefore, we return `true`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m):
    x, y = 0, 0
    for i in m:
        if (i == 'L'):
            x -= 1
        if (i == 'R'):
            x += 1
        if (i == 'U'):
            y += 1
        if (i == 'D'):
            y -= 1

    return (x, y) == (0, 0)
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
[leetcode.com](https://leetcode.com/problems/robot-return-to-origin/)
