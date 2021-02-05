#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given an array `a`, write a function to move all `0`'s to the end of it while maintaining the relative order of the non-zero elements.
#### Sample Input :point_down:
```
a = [0, 1, 0, 3, 12]
```
#### Sample Output :point_down:
```
1 3 12 0 0
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    c = 0
    for i in range(len(nums)):
        if (nums[i] != 0):
            nums[c] = nums[i]
            c += 1

    while (c < len(nums)):
        nums[c] = 0
        c += 1
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
[geeksforgeeks.org](https://www.geeksforgeeks.org/move-zeroes-end-array/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/move-zeroes/)
