#### Topics :point_down:
![](https://img.shields.io/badge/-prime--factors-wheat)

#### Problem :point_down:
Given a integer `n`, determine whether `n` is an ugly number.  
Ugly numbers are `positive numbers` whose prime factors only include `2, 3, 5`.  
Note: `1` is typically treated as an ugly number.
#### Sample Input :point_down:
```
n = 12
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`12 = 2 x 2 x 3`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(num):
    if (num <= 0):
        return False

    if (num == 1):
        return True

    while (num % 2 == 0):
        num //= 2

    while (num % 3 == 0):
        num //= 3

    while (num % 5 == 0):
        num //= 5

    if (num == 1):
        return True

    return False
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/print-all-prime-factors-of-a-given-number/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/ugly-number/)
