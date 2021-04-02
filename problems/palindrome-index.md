#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a string `s` of lowercase letters, determine the index of a character that can be removed to make the string a palindrome. There may be more than one solution, but any will do. If the word is already a palindrome or there is no solution, return `-1`. Otherwise, return the index of a character to remove. 
#### Sample Input :point_down:
```
s = "bcbc"
```
#### Sample Output :point_down:
```
0
```
#### Explanation :point_down:
If `s[0]` is removed, `s = "cbc"`, which is palindrome.  
`3` is also a valid answer, because if `s[3]` is removed, `s = "bcb"`, which is also palindrome.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(s):
    if s[::-1] == s:
        return -1
    
    i, j = 0, len(s)-1
    while i < j:
        if s[i] != s[j]:
            break
        i += 1
        j -= 1
                
    t = ''.join([s[k] for k in range(len(s)) if k != i])
    if t[::-1] == t:
        return i
    
    t = ''.join([s[k] for k in range(len(s)) if k != j])
    if t[::-1] == t:
        return j

    return -1
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
[hackerrank.com](https://www.hackerrank.com/challenges/palindrome-index/problem)
