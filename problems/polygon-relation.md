#### Topics :point_down:
![](https://img.shields.io/badge/-geometry-wheat) ![](https://img.shields.io/badge/-greedy-wheat)

#### Problem :point_down:
You are given a strictly convex polygon with n vertices. You may perform the following operation any number of times (including zero):
- Consider a parent polygon. Initially, this is the polygon you are given.
- Draw one of its child polygons ― a simple non-degenerate polygon such that each of its sides is a chord of the parent polygon (it cannot be a side of the parent polygon). The operation cannot be performed if the parent polygon does not have any child polygons.
- The child polygon which you drew becomes the new parent polygon.

Your goal is to draw as many sides of polygons in total as possible (including the polygon given at the start). Find total number of sides such that `total number of sides` are `maximum`.
#### Sample Input :point_down:
```
n = 8
```
#### Sample Output :point_down:
```
12
```
#### Explanation :point_down:

<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/polygon.png" height="150">

Originally given polygon of 8 sides and newly drawn child polygon of 4 side, makes total of 12 sides.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    total_sides = n
    while (n > 5):
        n //= 2
        total_sides += n

    return total_sides
```
</details>

#### Reference :point_down:
[codechef.com](https://discuss.codechef.com/problems/POLYREL)

#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/POLYREL)
