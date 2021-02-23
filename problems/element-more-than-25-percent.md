#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 

#### Problem :point_down:
Given an integer array `a` sorted in non-decreasing order, there is exactly one integer in the array that occurs `more than 25%` of the time. Return that integer.
#### Sample Input :point_down:
```
a = [1, 2, 2, 6, 6, 6, 6, 7, 10]
```
#### Sample Output :point_down:
```
6
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    for i in d:
        if (d[i] * 4) > len(a):
            return i
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
    c = 1 # count
    for i in range(1, n):
        if a[i] == a[i-1]:
            c += 1
        else:
            c = 1

        if (c * 4) > n:
            return a[i]

    return a[0]
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
[leetcode.com](https://leetcode.com/problems/element-appearing-more-than-25-in-sorted-array/submissions/)
