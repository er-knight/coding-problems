#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of numbers `a`. A sequence of numbers is called an arithmetic progression if the difference between any two consecutive elements is the same.  
Return `true` if the array can be rearranged to form an arithmetic progression, otherwise, return `false`.
#### Sample Input :point_down:
```
a = [3, 5, 1]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can reorder the elements as `[1,3,5]` or `[5,3,1]` with differences `2` and `-2` respectively, between each consecutive elements.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    a.sort()
    d = a[1] - a[0]
    for i in range(2, len(a)):
        if (a[i] - a[i-1]) != d:
            return False

    return True
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

#### Reference :point_down:

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/can-make-arithmetic-progression-from-sequence/)
