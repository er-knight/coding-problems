#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given two lowercase alphabet strings `s` and `t`, both of them the same length. You can pick one character in `s` and another in `t` and swap them. Given you can make unlimited number of swaps, return whether it's possible to make the two strings equal.
#### Sample Input :point_down:
```
s = "ab"
t = "ba"
```
#### Sample Output :point_down:
```
True
```
#### Explanation :point_down:
swap `s[0]` and `t[0]`.
```
s = "bb"
t = "aa"
```
swap `s[0]` and `t[1]`.
```
s = "ab"
t = "ab"
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    d = {}
    for i in s:
        d[i] = d.get(i, 0) + 1
    for i in t:
        d[i] = d.get(i, 0) + 1
        
    for i in d.values():
        if i % 2 != 0:
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
#### Python :point_down:
```py
def solve(s, t):
    s = sorted(s + t)
    c = 1
    for i in range(1, len(s)):
        if s[i] == s[i-1]:
            c += 1
        else:
            if c % 2 != 0:
                return False
            c = 1

    return True
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Swap-Characters-to-Equalize-Strings)
