#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You wish to buy video games from the famous online video game store. Usually, all games are sold at the same price, `p` dollars. However, they are planning to have the seasonal Halloween Sale next month in which you can buy games at a cheaper price. Specifically, the first game will cost `p` dollars, and every subsequent game will cost `d` dollars less than the previous one. This continues until the cost becomes less than or equal to `m` dollars, after which every game will cost `m` dollars. How many games can you buy during the Halloween Sale if you have `s` dollars initially?
#### Sample Input :point_down:
```
p = 20
d = 3
m = 6
s = 85
```
#### Sample Output :point_down:
```
7
```
#### Explanation :point_down:
Start at `p = 20` units cost, then reduce `p` by `d = 3` units each iteration until reaching a minimum possible price `m = 6`.
You can buy `7` games since they cost `20 + 17 + 14 + 11 + 8 + 6 + 6 = 82`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p, d, m, s):
    g = 0
    while s >= p:
        s -= p
        p = max(p - d, m)
        g += 1
    
    return g
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
o(1)
```
#### Python :point_down:
```py
def solve(p, d, m, s):
    if s < p:
        n = 0
    else:
        n = 1 + (p - m) // d
        t = n * (2 * p - (n - 1) * d) // 2
        if s >= t:
            n += (s - t) // m
        else:
            b = 2 * p + d
            n = int((b - sqrt(b * b - 8 * d * s)) / (2 * d))
    
    return n
```
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
o(1)
```
#### Reference :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/halloween-sale/forum/comments/459255)
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/halloween-sale/problem)
