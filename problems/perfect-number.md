#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
A perfect number is a positive integer that is equal to the sum of its positive divisors, excluding the number itself. A divisor of an integer `n` is an integer that can divide `n` evenly.  
Given an integer `n`, return true if `n` is a perfect number, otherwise return false.
#### Sample Input :point_down:
```
28
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
```
28 = 1 + 2 + 4 + 7 + 14
```
`1`, `2`, `4`, `7`, and `14` are all divisors of `28`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    if (n == 1):
        return False

    d = [1]
    for i in range(2, int(sqrt(n)) + 1):
        if (n % i == 0):
            d.append(i)
            d.append(n//i)

    return sum(d) == n
```  
#### Time Complexity :point_down:
```
O(sqrt(n))
```
#### Space Complexity :point_down:
```
O(sqrt(n))
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/perfect-number/)
