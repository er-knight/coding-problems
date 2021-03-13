#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
There is a string `s` of lowercase English letters that is repeated infinitely many times. Given an integer `n`, find the number of letter `a`'s in the first `n` letters of the infinite string.
#### Sample Input :point_down:
```
s = "aba"
n = 10
```
#### Sample Output :point_down:
```
7
```
#### Explanation :point_down:
first `n = 10` letters of infinite string are `"abaabaabaa"` and there are `7` `a`'s in it.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, n):    
    return (s.count('a') * (n // len(s)) + s[:n % len(s)].count('a'))
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
[hackerrank.com](https://www.hackerrank.com/challenges/repeated-string/problem)
