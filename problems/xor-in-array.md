#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
Given an integer `n` and an integer `s`.  
Define an array `a` where `a[i] = s + 2*i` (0-indexed) and `n == length of array`.  
Return the bitwise XOR of all elements of `a`.
#### Sample Input :point_down:
```
n = 4
s = 3
```
#### Sample Output :point_down:
```
8
```
#### Explanation :point_down:
```
a = [3, 5, 7, 9], where (3 ^ 5 ^ 7 ^ 9) = 8.
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, s):
    x = 0 # xor
    for i in range(n):
        x ^= s + 2 * i

    return x
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
[leetcode.com](https://leetcode.com/problems/xor-operation-in-an-array/)
