#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`, consisting of digits and lowercase alphabet characters, that's a run-length encoded string, return its decoded version.
#### Sample Input :point_down:
```
s = "4a3b2c1d2a"
```
#### Sample Output :point_down:
```
"aaaabbbccdaa"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    t = []
    n = 0
    for i in s:
        if i.isdigit():
            n = n * 10 + int(i)
        else:
            t.extend([n, i])
            n = 0

    e = ''
    for i in range(0, len(t), 2):
        e += (t[i] * t[i+1])

    return e
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
[binarysearch.com](https://binarysearch.com/problems/Run-Length-Decoding)
