#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
You are given a string `s` containing lowercase and uppercase alphabet characters as well as digits from `"0"` to `"9"`. Return whether `s` is a palindrome if we only consider the lowercase alphabet characters.
#### Sample Input :point_down:
```
s = "a92bcbXa"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
If we only consider the lowercase characters, then `s` is `"abcba"` which is a palindrome.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(s):
    t = ''
    for c in s:
        if c.islower():
            t += c

    return t == t[::-1]
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
    i, j = 0, len(s)-1
    while i < j:
        if s[i].islower() and s[j].islower():
            if s[i] != s[j]:
                return False
            i += 1
            j -= 1
        elif not s[i].islower():
            i += 1
        else:
            j -= 1

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
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Noisy-Palindrome)
