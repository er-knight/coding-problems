#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`, the power of the string is the maximum length of a non-empty substring that contains only one unique character.  
Return the power of the string.
#### Sample Input :point_down:
```
s = "leetcode"
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
The substring `"ee"` is of length `2` with the character `'e'` only.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    c = 1 # count
    t = 1 # temp
    for i in range(1, len(s)):
        if (s[i] == s[i-1]):
            t += 1
        else:
            t = 1

        c = max(c, t)

    return c
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
[leetcode.com](https://leetcode.com/problems/consecutive-characters/)
