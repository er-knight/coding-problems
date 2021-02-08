#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given two strings `s` and `t`, check if `s` is a subsequence of `t`.  
A subsequence of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. (i.e., `"ace"` is a subsequence of `"abcde"` while `"aec"` is not).
#### Sample Input :point_down:
```
s = "abc"
t = "ahbgdc"
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
    i = 0
    j = 0
    while (i < len(s) and j < len(t)):
        if (s[i] == t[j]):
            i += 1
        j += 1

    if (i < len(s)):
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

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/is-subsequence/)
