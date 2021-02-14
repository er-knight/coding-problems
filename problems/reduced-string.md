#### Topics :point_down:
![](https://img.shields.io/badge/-stack-wheat)
![](https://img.shields.io/badge/-string-wheat)
#### Problem :point_down:
Reduce a string of lowercase characters in range `ascii['a'..'z']` by doing a series of operations. In each operation, select a pair of adjacent letters that match, and delete them.  
Delete as many characters as possible using this method and return the resulting string. If the final string is empty, return `Empty String`.
#### Sample Input :point_down:
```
s = "aaabccddd"
```
#### Sample Output :point_down:
```
abd
```
#### Explanation :point_down:
Perform the following sequence of operations to get the final string.
```
aaabccddd → abccddd → abddd → abd
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    t = [] # stack
    for i in range(len(s)):
        if (not(t)):
            t.append(s[i])
        elif (t[-1] == s[i]):
            t.pop()
        else:
            t.append(s[i])
            
    return ''.join(t) if (t) else 'Empty String'
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
[hackerrank.com](https://www.hackerrank.com/challenges/reduced-string/problem)
