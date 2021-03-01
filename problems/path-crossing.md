#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string path `p`, where `p[i] = 'N', 'S', 'E' or 'W'`, each representing moving one unit `north`, `south`, `east`, or `west`, respectively. You start at the origin `(0, 0)` on a 2D plane and walk on the path specified by path.  
Return `true` if the path crosses itself at any point, that is, if at any time you are on a location you've previously visited. Return `false` otherwise.
#### Sample Input :point_down:
```
p = "NESWW"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
<img src="https://assets.leetcode.com/uploads/2020/06/10/screen-shot-2020-06-10-at-123843-pm.png" width="250">
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p):
    d = {'00': True}
    x, y = 0, 0
    for i in p:
        if i == 'N':
            y += 1
            t = str(x) + str(y)
            if d.get(t, False):
                return True
            d[t] = True
        elif i == 'S':
            y -= 1
            t = str(x) + str(y)
            if d.get(t, False):
                return True
            d[t] = True
        elif i == 'E':
            x += 1
            t = str(x) + str(y)
            if d.get(t, False):
                return True
            d[t] = True
        else:
            x -= 1
            t = str(x) + str(y)
            if d.get(t, False):
                return True
            d[t] = True

    return False
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
def solve(p):
    v = set() # visited
    x, y = 0, 0
    v.add((x, y))
    for i in p:
        if i == 'N':
            y += 1
            if (x, y) in v:
                return True
            v.add((x, y))
        elif i == 'S':
            y -= 1
            if (x, y) in v:
                return True
            v.add((x, y))
        elif i == 'E':
            x += 1
            if (x, y) in v:
                return True
            v.add((x, y))
        else:
            x -= 1
            if (x, y) in v:
                return True
            v.add((x, y))

    return False
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
[leetcode.com](https://leetcode.com/problems/path-crossing/)
