#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-prefix--product-wheat) 

#### Problem :point_down:
Given an integer array `a`, return an array `b` such that `b[i]` is equal to the product of all the elements of `a` except `a[i]`.
#### Sample Input :point_down:
```
a = [1, 2, 3, 4]
```
#### Sample Output :point_down:
```
[24, 12, 8, 6]
```
#### Explanation :point_down:
```
👉 a[0] = a[1] * a[2] * a[3] = 2 * 3 * 4 = 24
👉 a[1] = a[0] * a[2] * a[3] = 1 * 3 * 4 = 12
👉 a[2] = a[0] * a[1] * a[3] = 1 * 2 * 4 = 8
👉 a[3] = a[0] * a[1] * a[2] = 1 * 2 * 3 = 6
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    n = len(a)

    l = [i for i in a] # left prefix product
    for i in range(1, n):
        l[i] *= l[i-1]

    r = [i for i in a] # right prefix product
    for i in range(n-2, -1, -1):
        r[i] *= r[i+1]            

    for i in range(n):
        if i == 0:
            a[i] = r[i+1]
        elif i == n-1:
            a[i] = l[i-1]
        else:
            a[i] = l[i-1] * r[i+1]

    return a
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(a):
    n = len(a)
    b = [] # output

    p = 1
    for i in range(n):
        b.append(p)
        p = p * a[i]

    p = 1
    for i in range(n-1, -1, -1):
        b[i] = b[i] * p
        p = p * a[i]

    return b
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
The output array does not count as extra space for space complexity analysis.
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/product-of-array-except-self/)
