#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 

#### Problem :point_down:
Given an integer `n`. Each number from `1` to `n` is grouped according to the sum of its digits. 
Return how many groups have the largest size.
#### Sample Input :point_down:
```
n = 13
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
There are `9` groups in total, they are grouped according sum of its digits of numbers from `1` to `13`:
```
[1, 10], [2, 11], [3, 12], [4, 13], [5], [6], [7], [8], [9]. 
```
There are `4` groups with largest size i.e., `2`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    d = {}
    m = 0
    for i in range(1, n+1):
        s = 0
        while i:
            s += (i % 10)
            i //= 10

        d[s] = d.get(s, 0) + 1
        m = max(m, d[s])

    c = 0
    for i in d:
        if d[i] == m:
            c += 1

    return c
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/count-largest-group/)
