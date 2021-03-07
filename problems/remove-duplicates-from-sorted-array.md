#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a sorted array `a`, remove the duplicates in-place such that each element appears only once and returns the new length.  
Do not allocate extra space for another array, you must do this by modifying the input array in-place with `O(1)` extra memory.
#### Sample Input :point_down:
```
a = [0, 0, 1, 1, 1, 2, 2, 3, 3, 4]
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
```
a = [0, 1, 2, 3, 4]
a.length = 5
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    if not a:
        return 0

    k = 1
    for i in range(1, len(a)):
        if a[i] != a[i-1]:
            a[k] = a[i]
            k += 1

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
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
