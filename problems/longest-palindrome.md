#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat) ![](https://img.shields.io/badge/-palindrome-wheat) ![](https://img.shields.io/badge/-hashmap-wheat)

#### Problem :point_down:
Given a string `s` which consists of lowercase or uppercase letters, return the length of the longest palindrome that can be built with those letters.  
Letters are case sensitive, for example, `"Aa"` is not considered a palindrome here.
#### Sample Input :point_down:
```
s = "abccccdd"
```
#### Sample Output :point_down:
```
7
```
#### Explanation :point_down:
One longest palindrome that can be built is `"dccaccd"`, whose length is `7`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    m = {}
    for i in s:
        m[i] = m.get(i, 0) + 1

    l = 0 # length
    f = 0 # odd flag

    for i in m.values():
        if (i % 2 == 1):
            f = 1
        l += (i // 2) * 2

    return l + f
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
def solve(s):
    a = set()
    c = 0 # count
    for i in s:
        if i in a:
            a.remove(i)
            c += 1
        else:
            a.add(i)

    return 2 * c + (1 if a else 0)
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
[leetcode.com](https://leetcode.com/problems/longest-palindrome/)
