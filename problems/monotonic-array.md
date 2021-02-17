#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
An array is monotonic if it is either monotone increasing or monotone decreasing.  
An array `a` is monotone increasing if for all `i <= j`, `a[i] <= a[j]`. An array `a` is monotone decreasing if for all `i <= j`, `a[i] >= a[j]`.  
Return `true` if and only if the given array `a` is monotonic.
#### Sample Input :point_down:
```
a = [1, 2, 2, 3]
```
#### Sample Output :point_down:
```
true
```  

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    is_monotonic_increasing = True
    is_monotonic_decreasing = True   

    for i in range(1, len(a)):
        if (a[i-1] > a[i]):
            is_monotonic_increasing = False
        if (a[i-1] < a[i]):
            is_monotonic_decreasing = False

    return is_monotonic_increasing or is_monotonic_decreasing
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
[leetcode.com](https://leetcode.com/problems/monotonic-array/)
