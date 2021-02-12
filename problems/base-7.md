#### Topics :point_down:
![](https://img.shields.io/badge/-base--conversion-wheat) 

#### Problem :point_down:
Given an integer `n`, return its `base 7` string representation.
#### Sample Input :point_down:
```
100
```
#### Sample Output :point_down:
```
202
```
#### Explanation :point_down:
`100` in `base 10` is representated as `202` in `base 7`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    if not(n):
        return '0'

    f = True if (n < 0) else False # flag
    n = abs(n)
    s = ''
    while (n):
        s += str(n % 7)
        n //= 7

    if (f):
        return '-' + s[::-1]

    return s[::-1]
```  
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/base-7/)
