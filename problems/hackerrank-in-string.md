#### Topics :point_down:
![](https://img.shields.io/badge/-queue-wheat)
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a string `s`, return whether it's possible to pick some subsequence of characters in `s` such that the characters form the string `"hackerrank"`.
#### Sample Input :point_down:
```
s = "hereiamstackerrank"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
```
h e r e i a m s t a c k e r r a n k
↑                 ↑ ↑ ↑ ↑ ↑ ↑ ↑ ↑ ↑
```
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(s):
    t = 'hackerrank'
    j = 0
    for i in range(len(s)):
        if j < len(t) and s[i] == t[j]:
            j += 1
            
    if j < len(t):
        return False
    
    return True
```  
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(s):
    q = list('hackerrank') # queue
    for c in s:
        if q and c == q[0]:
            q.pop(0)
        if not q:
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
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/hackerrank-in-a-string/problem)
