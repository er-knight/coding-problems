#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a string `s` and an integer `k`, rearrange `s` into `k` rows so that `s` can be read vertically (top-down, left to right).
#### Sample Input :point_down:
```
s = "abcdefghi"
k = 5
```
#### Sample Output :point_down:
```
["af", "bg", "ch", "di", "e"]
```
#### Explanation :point_down:
This reads vertically as:
```
["af",
 "bg",
 "ch",
 "di",
 "e"]
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, k):
    c = [] # cipher
    for i in range(k):
        t = '' # temp
        for j in range(i, len(s), k):
            t += s[j]
        c.append(t)

    return c
```  
#### Time Complexity :point_down:
```
O(k * (len(s) % k))
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Vertical-Cipher)
