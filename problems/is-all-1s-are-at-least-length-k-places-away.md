#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given an array `a` of `0`s and `1`s and an integer `k`, return `true` if all `1`'s are at least `k` places away from each other, otherwise return `false`.
#### Sample Input :point_down:
```
a = [1, 0, 0, 0, 1, 0, 0, 1]
k = 2
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
<img src="https://assets.leetcode.com/uploads/2020/04/15/sample_1_1791.png" width="200">
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = 0            
    for i in range(len(a)):
        if (a[i] == 1):
            break
        d += 1

    for i in range(d+1, len(a)):
        if a[i] == 1:
            if (i - d) <= k:
                return False
            d = i

    return True
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
[leetcode.com](https://leetcode.com/problems/check-if-all-1s-are-at-least-length-k-places-away/)
