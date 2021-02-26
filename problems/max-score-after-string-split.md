#### Topics :point_down:
![](https://img.shields.io/badge/-prefix--sum-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s` of zeros and ones, return the maximum score after splitting the string into two non-empty substrings (i.e. left substring and right substring).  
The score after splitting a string is the number of zeros in the left substring plus the number of ones in the right substring.
#### Sample Input :point_down:
```
s = "011101"
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
All possible ways of splitting `s` into two non-empty substrings are:
```
left = "0"     and right = "11101" score = 1 + 4 = 5 
left = "01"    and right = "1101"  score = 1 + 3 = 4 
left = "011"   and right = "101"   score = 1 + 2 = 3 
left = "0111"  and right = "01"    score = 1 + 1 = 2 
left = "01110" and right = "1"     score = 2 + 1 = 3
```
<details>
<summary>Expand</summary>
  
#### Python :point_down:
```py
def solve(s):
    o = 0 
    z = [0 for i in range(len(s))]

    if s[0] == '0':
        z[0] = 1

    m = 0 # max score

    for i in range(1, len(s)):
        if s[i] == '0':
            z[i] += 1
        z[i] += z[i-1]

    for i in range(len(s)-1, 0, -1):
        if s[i] == '1':
            o += 1
        m = max(m, o + z[i-1])

    return m                
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
    z =  0           # zeroes
    o = s.count('1') # ones

    m = 0 # max score
    for i in range(len(s)-1):
        if s[i] == '0':
            z += 1
        else:
            o -= 1

        m = max(m, z + o)

    return m
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
[leetcode.com](https://leetcode.com/problems/maximum-score-after-splitting-a-string/)
