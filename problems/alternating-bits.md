#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-modulus-wheat) 
![](https://img.shields.io/badge/-stack-wheat)

#### Problem :point_down:
Given a positive integer `n`, check whether it has alternating bits: namely, if two adjacent bits will always have different values.
#### Sample Input :point_down:
```
n = 5
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
The binary representation of 5 is `101`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    stack = []
    stack.append(n % 2)
    n //= 2
    while (n):
        if (stack[-1] == (n % 2)):
            return False
        stack.append(n % 2)
        n //= 2

    return True
```  
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(log n)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/binary-number-with-alternating-bits/)
