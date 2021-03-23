#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s` consisting of only `1`s and `0`s, find the number of substrings which start and end both in `1`.
In this problem, a substring is defined as a sequence of continuous characters `s[i]`, `s[i+1]`, ..., `s[j]` where `1 ≤ i ≤ j ≤ n`. 
#### Sample Input :point_down:
```
s = "1111"
```
#### Sample Output :point_down:
```
10
```
#### Explanation :point_down:
```
s[0] = "1"
s[1] = "1"
s[2] = "1"
s[3] = "1"
s[0] + s[1] = "11"
s[1] + s[2] = "11"
s[2] + s[3] = "11"
s[0] + s[1] + s[2] = "111"
s[1] + s[2] + s[3] = "111"
s[0] + s[1] + s[2] + s[3] = "1111"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    c = s.count('1')
    return (c * (c+1))//2
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
[codechef.com](https://www.codechef.com/problems/CSUB)
