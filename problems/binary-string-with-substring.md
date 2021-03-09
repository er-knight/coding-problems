#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a binary string `s` (a string consisting only of `'0'` and `'1'`s) and a positive integer `n`, return `true` if and only if for every integer `x` from `1 to n`, the binary representation of `x` is a substring of `s`.
#### Sample Input :point_down:
```
s = "0110"
n = 3
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
```
1 in binary → "1"
2 in binary → "10"
3 in binary → "11"
```
For all integers `i` from `1 to 3`, `binary(i)` is in `"0110"`.
<details>
<summary>Expand</summary>

#### Python 👇
```py
def solve(s, n):
    for i in range(n, n//2, -1):
        if bin(i)[2:] not in s:
            return False

    return True
```
#### Hint 👇
For every `i < n/2`, binary string of `2 * i` will contain binary string of `i`. Thus we don't need to check for `i < n/2`.
#### Time Complexity 👇
```
O(n)
```
#### Space Complexity 👇
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/binary-string-with-substrings-representing-1-to-n/)
