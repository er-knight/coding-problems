#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given number of friends, `n` and array `t` representing number of toffees each friend wants, return minimum number of toffees needed to satisfy the condition of atleast one friend in any possible distribution of toffees i.e, atleast one friend must get as many toffees he wants.

#### Sample Input :point_down:
```
n = 3
t = [8, 6, 9]
```
#### Sample Output :point_down:
```
21
```
#### Explanation :point_down:
One of the distribution of `21` is `7 6 8`, which satifies second friend and every other distribution satifies atleast one friend.
If `20` toffees taken, one of the distribution of `20` toffees is `7 5 8` which will not satisfy any of them.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, t):
    return (sum(t) - (n - 1))
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
[hackerearth.com](https://www.hackerearth.com/problem/algorithm/candy-distribution-2/)
