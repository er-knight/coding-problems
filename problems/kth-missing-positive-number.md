#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat) 

#### Problem :point_down:
Given an array `a` of positive integers sorted in a strictly increasing order, and an integer `k`.  
Find the `kth` positive integer that is missing from this array.
#### Sample Input :point_down:
```
a = [2, 3, 4, 7, 11]
k = 5
```
#### Sample Output :point_down:
```
9
```
#### Explanation :point_down:
The missing positive integers are `[1, 5, 6, 8, 9, 10, 12, 13,...]`.  
The `5th` missing positive integer is `9`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, k):
    d = {}
    for i in a:
        d[i] = 1

    n = 0
    while k:
        n += 1 
        if not d.get(n):
            k -= 1

    return n
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
def solve(a, k):
    s = set(a)
    n = 0
    while k:
        n += 1 
        if n not in s:
            k -= 1

    return n
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
def solve(a, k):
    for i in a:
        if i <= k:
            k += 1 
        else:
            break

    return k
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
def solve(a, k):
    l, r = 0, len(a)
    while l < r:
        m = (l + r)//2
        if (a[m] - m - 1) < k:
            l = m + 1
        else:
            r = m

    return l + k
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Reference :point_down:
[leetcode.com](https://leetcode.com/problems/kth-missing-positive-number/discuss/1004535/Python-Two-solutions-O(n)-and-O(log-n)-explained)
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/kth-missing-positive-number/)
