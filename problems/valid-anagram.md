#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat) ![](https://img.shields.io/badge/-hashmap-wheat)

#### Problem :point_down:
Given two strings `s` and `t`, write a function to determine if `t` is an anagram of `s`.
#### Sample Input :point_down:
```
s = "anagram"
t = "nagaram"
```
#### Sample Output :point_down:
```
true
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    m = [0] * 26 # mapping
    for i in s:
        m[ord(i) - 97] += 1
    for i in t:
        m[ord(i) - 97] -= 1
    for i in m:
        if (i != 0):
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
[leetcode.com](https://leetcode.com/problems/valid-anagram/)
