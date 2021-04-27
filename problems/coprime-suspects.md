#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given two integers, `a` and `b`. In each operation, you can choose either integer, and either increment it by `1` or decrement it by `1`.
What is the minimum number of operations you need such that the greatest common divisor between `a` and `b` is `≠ 1`?

Note that you are allowed to make `0` operations if no operations are needed.
#### Sample Input :point_down:
```
a = 3
b = 7
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
We can decrement `7` to `6` to get a greatest common divisor of `3`.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a, b):
    if gcd(a, b) > 1:
        return 0

    if gcd(a-1, b) > 1 or gcd(a, b-1) > 1 or gcd(a+1, b) > 1 or gcd(a, b+1) > 1:
        return 1

    return 2
```  
#### Hint :point_down:
```
👉 Any two even number will have gcd > 1
```
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Coprime-Suspects)
