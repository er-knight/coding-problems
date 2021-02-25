#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
Given a non-negative integer `n`, return the number of steps to reduce it to zero. If the current number is even, you have to divide it by `2`, otherwise, you have to subtract `1` from it.
#### Sample Input :point_down:
```
n = 14
```
#### Sample Output :point_down:
```
8
```
#### Explanation :point_down:
```
step 1) 14 is even, divide by 2 and obtain 7. 
step 2)  7 is  odd, subtract 1 and obtain 6.
step 3)  6 is even, divide by 2 and obtain 3. 
step 4)  3 is  odd, subtract 1 and obtain 2. 
step 5)  2 is even, divide by 2 and obtain 1. 
step 6)  1 is  odd, subtract 1 and obtain 0.
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    c = 0
    while (n):
        if n % 2 == 0:
            n //= 2
        else:
            n -= 1
        c += 1
    return c
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
    return int(math.log2(n)) + bin(n).count('1') if n else 0
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
    n = bin(n)[2:]
    return len(n) - 1 + n.count('1') if n else 0
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/number-of-steps-to-reduce-a-number-to-zero/)
