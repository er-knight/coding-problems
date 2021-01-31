#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given an array `a` of size `n` where every element is in the range from `0 to n-1`, rearrange it so that `a[i]` becomes `a[a[i]]`.
#### Sample Input :point_down:
```
n = 4
a = [3, 2, 0, 1]
```
#### Sample Output :point_down:
```
[1, 0, 3, 2]
```
#### Explanation :point_down:
```
In given array, 
a[a[0]] is 1, so a[0] in output array is 1
a[a[1]] is 0, so a[1] in output array is 0
a[a[2]] is 3, so a[2] in output array is 3
a[a[3]] is 2, so a[3] in output array is 2
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, n):
    b = [0] * n
    for i in range(n):
        b[i] = a[a[i]]

    return b
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
def solve(a, n):
    for i in range(n):
        a[i] += (a[a[i]] % n) * n

    for i in range(n):
        a[i] //= n

    return a
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/rearrange-given-array-place/)
#### Solve Here :point_down:
[geeksforgeeks.org](https://practice.geeksforgeeks.org/problems/rearrange-an-array-with-o1-extra-space3142/1)
