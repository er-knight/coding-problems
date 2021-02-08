#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string, find the first non-repeating character in it and return its index. If it doesn't exist, return -1.
#### Sample Input :point_down:
```
s = "leetcode"
```
#### Sample Output :point_down:
```
0
```
#### Explanation :point_down:
`'l', 't', 'c', 'o', 'd'` are non-repeating characters where `'l'` has minimum index `0`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    m = [[] for _ in range(26)] # mapping

    for i, c in enumerate(s):
        m[ord(c) - 97].append(i) 

    # unique characters index
    u = [i[0] for i in m if len(i) == 1]

    return min(u) if u else -1 
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
[leetcode.com](https://leetcode.com/problems/first-unique-character-in-a-string/)
