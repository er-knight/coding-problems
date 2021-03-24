#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-greedy-wheat)
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Chef has gone shopping with his 5-year old son. They have bought `n` items so far. The items are numbered from `1` to `n`, and the item `i` weighs `w[i]` grams.

Chef's son insists on helping his father in carrying the items. He wants his dad to give him a few items. Chef does not want to burden his son. But he won't stop bothering him unless he is given a few items to carry. So Chef decides to give him some items. Obviously, Chef wants to give the kid less weight to carry.

However, his son is a smart kid. To avoid being given the bare minimum weight to carry, he suggests that the items are split into two groups, and one group contains exactly `k` items. Then Chef will carry the heavier group, and his son will carry the other group.

Help the Chef in deciding which items should the son take. Your task will be simple. Tell the Chef the maximum possible difference between the weight carried by him and the weight carried by the kid. 
#### Sample Input :point_down:
```
n = 5
k = 2
w = [8, 4, 5, 2, 10]
```
#### Sample Output :point_down:
```
17
```
#### Explanation :point_down:
Chef gives his son `k = 2` items with weights `2` and `4`. Chef carries the rest of the items himself.  
Thus the difference is `(8 + 5 + 10) − (4 + 2) = 23 − 6 = 17`. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py

```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/MAXDIFF)
