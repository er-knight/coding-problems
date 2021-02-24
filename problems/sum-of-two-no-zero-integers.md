#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer `n`. No-Zero integer is a positive integer which doesn't contain any `0` in its decimal representation.  
Return a list of two integers `[A, B]` where:
- `A` and `B` are No-Zero integers.
- `A + B = n`

It's guarateed that there is at least one valid solution. If there are many valid solutions you can return any of them.
#### Sample Input :point_down:
```
n = 11
```
#### Sample Output :point_down:
```
[2, 9]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    a, b = 1, n-1
    while ('0' in str(a)) or ('0' in str(b)):
        a += 1
        b -= 1

    return [a, b]
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
[leetcode.com](https://leetcode.com/problems/convert-integer-to-the-sum-of-two-no-zero-integers/)
