#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a string `s` containing `"0"`s and `"1"`s, consider an operation where you pick a character and toggle its value from `"0"` to `"1"` or from `"1"` to `"0"`. Return the minimum number of operations required to obtain a string containing no instances of three identical consecutive characters.
#### Sample Input :point_down:
```
s = "1100011"
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
We can toggle the middle `"0"` to a `"1"`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    if len(s) > 2:
        c = 1
        o = 0 # operations
        for i in range(1, len(s)):
            if s[i] == s[i-1]:
                c += 1
            else:
                o += c//3
                c = 1

        return o + c//3

    return 0
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
    return s.count('000') + s.count('111')
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
[binarysearch.com](https://binarysearch.com/problems/Removing-Triple-Successive-Duplicates)
