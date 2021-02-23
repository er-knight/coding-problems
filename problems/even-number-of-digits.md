#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-bit--manipulation-wheat)
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an array `a` of integers, return how many of them contain an even number of digits. 
#### Sample Input :point_down:
```
a = [12, 345, 2, 6, 7896]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
```
  12 contains 2 digits (even number of digits). 
 345 contains 3 digits (odd number of digits). 
   2 contains 1 digit  (odd number of digits). 
   6 contains 1 digit  (odd number of digits). 
7896 contains 4 digits (even number of digits). 
```
Therefore only `12` and `7896` contain an even number of digits.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    c = 0 # count
    for k in a:
        t = 0 # temp count
        while (k):
            t += 1
            k //= 10

        if (t % 2) == 0:
            c += 1

    return c
```
#### Time Complexity :point_down:
```
O(n log k)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    c = 0 # count
    for i in a:
        if (int(math.log10(i)) + 1) % 2 == 0:
            c += 1

    return c
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    c = 0 # count
    for i in a:
        if len(str(i)) % 2 == 0:
            c += 1

    return c
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
[leetcode.com](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)
