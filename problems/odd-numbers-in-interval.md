#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given two non-negative integers `l` and `h`. Return the count of odd numbers between `l` and `h` (inclusive).
#### Sample Input :point_down:
```
l = 3
h = 7
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
The odd numbers between `3` and `7` are `[3, 5, 7]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(l, h):
    return (h+1)//2 - l//2
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
[leetcode.com](https://leetcode.com/problems/count-odd-numbers-in-an-interval-range/)
