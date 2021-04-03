#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
Given a positive integer `n`, output its complement number. The complement strategy is to flip the bits of its binary representation.
#### Sample Input :point_down:
```
n = 5
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
The binary representation of `5` is `101` (no leading zero bits), and its complement is `010`. So, output is `2`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    c = ''
    while (n):
        c += '0' if (n % 2) else '1'
        n //= 2

    return int(c[::-1], base=2)
```  
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(log n)
```  
#### Python :point_down:
```py
def solve(n):
    l = int(math.log(n, 2)) + 1
    for i in range(l):
        n = (n ^ (1 << i))

    return n
```  
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(log n)
```  
#### Python :point_down:
```py
def solve(n):
    return 4294967295 - n
```  
#### Note :point_down:
This works only if `n` is 32-bit integer.
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/invert-actual-bits-number/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/number-complement/)  
[hackerrank.com](https://www.hackerrank.com/challenges/flipping-bits/problem)
