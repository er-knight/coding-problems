#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a string `s`, return the "reversed" string where all characters that are not a letter stay in the same place, and all letters reverse their positions.
#### Sample Input :point_down:
```
s = "a-bC-dEf-ghIj" 
```
#### Sample Output :point_down:
```
"j-Ih-gfE-dCba"
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    a = ''
    for i in s:
        if i.isalpha():
            a += i

    a = a[::-1]
    b = ''
    k = 0
    for i in s:
        if i.isalpha():
            b += a[k]
            k += 1
        else:
            b += i

    return b
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
    s = list(s)

    i = 0
    j = len(s)-1

    while (i < j):
        if s[i].isalpha() and s[j].isalpha():
            s[i], s[j] = s[j], s[i]
            i += 1
            j -= 1

        if not s[i].isalpha():
            i += 1

        if not s[j].isalpha():
            j -= 1

    return ''.join(s)
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
[leetcode.com](https://leetcode.com/problems/reverse-only-letters/)
