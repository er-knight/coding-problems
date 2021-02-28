#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given alphanumeric string `s`. Alphanumeric string is a string consisting of lowercase English letters and digits.  
You have to find a permutation of the string where no letter is followed by another letter and no digit is followed by another digit. That is, no two adjacent characters have the same type.  
Return the reformatted string or return an empty string if it is impossible to reformat the string.
#### Sample Input :point_down:
```
s = "ab123"
```
#### Sample Output :point_down:
```
"1a2b3"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    a = '' # alpha
    n = '' # numeric
    for i in s:
        if i.isalpha():
            a += i
        else:
            n += i

    if not(a) and len(n) == 1:
        return s

    if not(n) and len(a) == 1:
        return s

    if len(s) % 2 == 0 and len(a) == len(n):
        return ''.join([a[i] + n[i] for i in range(len(a))])

    if (len(a) - len(n)) == 1:
        return ''.join([a[i] + n[i] for i in range(len(n))]) + a[-1]

    if (len(n) - len(a)) == 1:
        return ''.join([n[i] + a[i] for i in range(len(a))]) + n[-1]      

    return ''
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
[leetcode.com](https://leetcode.com/problems/reformat-the-string/)
