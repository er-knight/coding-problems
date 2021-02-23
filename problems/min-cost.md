#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-greedy-wheat)
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
We have `n` chips, where the position of the `ith` chip is `p[i]`.  
We need to move all the chips to the same position.  
In one step, we can change the position of the `ith` chip from `p[i]` to:
- `p[i] + 2` or `p[i] - 2` with `cost = 0`.
- `p[i] + 1` or `p[i] - 1` with `cost = 1`.

Return the minimum cost needed to move all the chips to the same position.
#### Sample Input :point_down:
```
p = [1, 2, 3]
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
<img src="https://assets.leetcode.com/uploads/2020/08/15/chips_e1.jpg" width="500">
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p):            
    e = 0 # even
    o = 0 # odd

    for i in p:
        if i % 2 == 0:
            e += 1
        else:
            o += 1

    return min(e, o)
```
#### Time Complexity :point_down:
```
o(n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/minimum-cost-to-move-chips-to-the-same-position/)
