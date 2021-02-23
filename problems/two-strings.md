#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given two strings `s` and `t`, determine if they share a common substring. A substring may be as small as one character. 
#### Sample Input :point_down:
```
s = "hello"
t = "world"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
The substrings `"o"` and `"l"` are common to both strings. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    for i in s:
        if i in t:
            return True
        
    return False
```  
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(s, t):
    d = {}
    for i in s:
        d[i] = 1
        
    for i in t:
        if d.get(i, 0):
            return True
        
    return False
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
def solve(s, t):
    return set(s) & set(t)
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
[hackerrank.com](https://www.hackerrank.com/challenges/two-strings/problem)
