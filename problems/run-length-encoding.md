#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`, return its run-length encoding. You can assume the string to be encoded have no digits and consists solely of alphabetic characters.
#### Sample Input :point_down:
```
s = "aaaabbbccdaa"
```
#### Sample Output :point_down:
```
"4a3b2c1d2a"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    c = 1 # count
    e = '' # encoded
    for i in range(1, len(s)):
        if s[i] == s[i-1]:
            c += 1
        else:
            e += str(c) + s[i-1]
            c = 1
    e += str(c) + s[-1]

    return e
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
[binarysearch.com](https://binarysearch.com/problems/Run-Length-Encoding)
