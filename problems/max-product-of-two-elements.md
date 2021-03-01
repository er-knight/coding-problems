#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of integers `a`, you will choose two different indices `i` and `j` of that array. Return the maximum value of `(a[i]-1)*(a[j]-1)`. 
#### Sample Input :point_down:
```
a = [3, 4, 5, 2]
```
#### Sample Output :point_down:
```
12
```
#### Explanation :point_down:
If you choose the indices `i = 1` and `j = 2` (indexed from `0`), you will get the maximum value, i.e., 
```
= (a[1] - 1) * (a[2] - 1) 
= (4 - 1) * (5 - 1) 
= 3 * 4 
= 12
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    m = 0
    for i in range(len(a)):
        for j in range(i+1, len(a)):
            m = max(m, (a[i] - 1) * (a[j] - 1))

    return m
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    a.sort()
    return (a[-1] - 1) * (a[-2] - 1)
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    m, n = 0, 0
    for i in a:
        if i > m:
            n = m
            m = i
        elif m >= i > n:
            n = i

    return (m - 1) * (n - 1)
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
[leetcode.com](https://leetcode.com/problems/maximum-product-of-two-elements-in-an-array/)
