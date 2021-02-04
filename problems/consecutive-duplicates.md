#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`, consisting of `"X"` and `"Y"`s, delete the minimum number of characters such that there's no consecutive `"X"` and no consecutive `"Y"`.
#### Sample Input :point_down:
```
s = "YYYXYXX"
```
#### Sample Output :point_down:
```
"YXYX"
```
#### Explanation :point_down:
One solution is to delete the first two `"Y"`s and the last `"X"`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s):
    if (len(s) == 0):
        return s
    s_ = s[0]
    for i in range(1, len(s)):
        if (s[i] != s_[-1]):
            s_ += s[i]

    return s_
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
[binarysearch.com](https://binarysearch.com/problems/Consecutive-Duplicates)
