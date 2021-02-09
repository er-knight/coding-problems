#### Topics :point_down:
![](https://img.shields.io/badge/-binary--tree-wheat)

#### Problem :point_down:
Find the sum of all left leaves in a given binary tree.
#### Sample Input :point_down:
```
[3, 9, 20, null, null, 15, 7]
```
#### Sample Output :point_down:
```
24
```
#### Explanation :point_down:
```
     3
    / \
   9   20
  / \
15   7
```
There are two left leaves in the binary tree, with values 9 and 15 respectively.
```
9 + 15 = 24
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(root):
    if root is None:
        return 0 

    stack = [] # for DFS
    stack.append(root)

    sum_ = 0

    while stack:
        current = stack.pop()
        if current.left is not None:
            stack.append(current.left)
            
            if current.left.left is None and current.left.right is None:
                sum_ += current.left.val

        if current.right is not None:
            stack.append(current.right)

    return sum_
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/find-sum-left-leaves-given-binary-tree/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/sum-of-left-leaves/)
