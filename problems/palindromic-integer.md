#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a non-negative integer `n`, return whether it is a palindrome.  
Bonus: Can you solve it without using strings?
#### Sample Input :point_down:
```
121
```
#### Sample Output :point_down:
```
true
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    n = str(n)
    return n[::-1] == n
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
    r, t = 0, n
    while t:
        r = r * 10 + (t % 10)
        t //= 10

    return r == n
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
[binarysearch.com](https://binarysearch.com/problems/Palindromic-Integer)
