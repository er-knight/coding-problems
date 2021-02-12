#### Topics :point_down:
![](https://img.shields.io/badge/-stack-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s` containing only characters `'A'` and `'B'`. Return the minimum number of deletions required to change `s` into a string such that there are no matching adjacent characters.
#### Sample Input :point_down:
```
s = "AABAAB"
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Remove an `'A'` at positions `0` and `3` to make `s = "ABAB"` in `2` deletions.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    t = [s[0]] # stack
    d = 0      # deletions
    for i in range(1, len(s)):
        if (t[-1] == s[i]):
            d += 1
        else:
            t.append(s[i])
            
    return d
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
    d = 0 # deletions
    for i in range(1, len(s)):
        if (s[i-1] == s[i]):
            d += 1
            
    return d
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
[hackerrank.com](https://www.hackerrank.com/challenges/alternating-characters/problem)
