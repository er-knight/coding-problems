#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Determine whether a string `s` is funny or not. To determine whether a string is funny, create a copy of the string in reverse  
e.g. `"abc" → "cba"`. Iterating through each string, compare the absolute difference in the ascii values of the characters at positions `0` and `1`, `1` and `2` and so on to the end. If the list of absolute differences is the same for both strings, they are funny.
#### Sample Input :point_down:
```
s = "acxz"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
```
s = "acxz"
r = "zxca"
```
Corresponding `ascii` values of characters of the strings:
```
s = [97, 99, 120, 122]
r = [122, 120, 99, 97]
```
For both the strings the adjacent difference list is `[2, 21, 2]`. 
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(s):
    for i in range(1, len(s)):
        a = abs(ord(s[i]) - ord(s[i-1]))
        b = abs(ord(s[-i]) - ord(s[-i-1]))
        if a != b:
            return False
        
    return True
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
[hackerrank.com](https://www.hackerrank.com/challenges/funny-string/problem)
