#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given lowercase alphabet strings `s` and `t`, return whether you can create a `1-to-1` mapping for each letter in `s` to another letter (could be the same letter) such that `s` could be mapped to `t`, with the ordering of characters preserved.
#### Sample Input :point_down:
```
s = "coco"
t = "kaka"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can create this mapping
```
"c" → "k"
"o" → "a"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    if (len(s) != len(t)):
        return False
        
    u = {}
    for i, c in enumerate(s):
        u[c] = u.get(c, []) + [i]
        
    v = {}
    for i, c in enumerate(t):
        v[c] = v.get(c, []) + [i]

    if (len(u) != len(v)):
        return False

    u = list(u.values())
    v = list(v.values())
    
    for i in range(len(u)):
        if (u[i] != v[i]):
            return False

    return True
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
[binarysearch.com](https://binarysearch.com/problems/String-Isomorphism)
