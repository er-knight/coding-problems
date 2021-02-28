#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given an integer `n`, return a string with `n` characters such that each character in such string occurs an odd number of times.  
The returned string must contain only lowercase English letters. If there are multiples valid strings, return any of them.  
#### Sample Input :point_down:
```
n = 4
```
#### Sample Output :point_down:
```
"pppz"
```
#### Explanation :point_down:
`"pppz"` is a valid string since the character `'p'` occurs three times and the character `'z'` occurs once.  
Note that there are many other valid strings such as `"ohhh"` and `"aaab"`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    return 'a' * n if (n % 2 == 1) else 'a' * (n-1) + 'b'
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
[leetcode.com](https://leetcode.com/problems/generate-a-string-with-characters-that-have-odd-counts/)
