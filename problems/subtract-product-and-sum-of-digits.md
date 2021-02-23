#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer number `n`, return the difference between the product of its digits and the sum of its digits. 
#### Sample Input :point_down:
```
n = 234 
```
#### Sample Output :point_down:
```
15
```
#### Explanation :point_down:
```
Product of digits = 2 * 3 * 4 = 24 
Sum of digits     = 2 + 3 + 4 = 9 
Result            = 24 - 9 = 15
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    p = 1 # product
    s = 0 # sum
    while (n):
        p *= (n % 10)
        s += (n % 10)
        n //= 10

    return (p - s)
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(n):
    return reduce(lambda x, y: x*y, (int(i) for i in str(n))) - sum((int(i) for i in str(n)))
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/subtract-the-product-and-sum-of-digits-of-an-integer/)
