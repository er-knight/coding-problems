#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
You are given two strings `t` (typed) and `r` (required). You want to write `r`, but the keyboard is stuck so some characters may be written `1` or more times. Return whether it's possible that `t` was meant to write `r`.
#### Sample Input :point_down:
```
t = "aaabcccc"
r = "abc"
```
#### Sample Output :point_down:
```
true
```
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(t, r):
    m = len(t)
    n = len(r)
    i, j = 0, 0
    while(i < n and j < m):
        if r[i] == t[j]:
            c, d = 0, 0
            s = r[i]
            i += 1
            while(i < n and r[i] == s):
                i += 1
                c += 1
            s = t[j]
            j += 1
            while(j < m and t[j] == s):
                d += 1
                j += 1
            if c > d:
                return False
        else:
            return False

    if i >= n and j >= m:
        return True

    return False
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
[binarysearch.com](https://binarysearch.com/problems/Stuck-Keyboard)
