#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given an array of positive integers `a`, return the number of integers that have odd number of digits.
#### Sample Input :point_down:
```
a = [1, 800, 2, 10, 3]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
`1`, `800`, `2` and `3` has odd number of digits.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, a):
    c = 0 # count
    for i in a:
        t = 0
        while i:
            t += 1
            i //= 10
        if t % 2 == 1:
            c += 1

    return c
```
#### Time Complexity :point_down:
```
o(n * log(i))
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(self, a):
    c = 0 # count
    for i in a:
        if int(log10(i) + 1) % 2 == 1:
            c += 1

    return c
```
#### Time Complexity :point_down:
```
o(n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(self, a):
    c = 0 # count
    for i in a:
        if len(str(i)) % 2 == 1:
            c += 1

    return c
```
#### Time Complexity :point_down:
```
o(n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Odd-Number-of-Digits)
