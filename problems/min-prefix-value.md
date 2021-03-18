#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-prefix--sum-wheat) 

#### Problem :point_down:
You are given an array of integers `a`. Return the minimum positive value we can append to the beginning of nums such that prefix sums of the resulting array contains numbers that are all greater than 0.
#### Sample Input :point_down:
```
a = [2, -5, 3, 2]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
If we have append `4` to the list then we have `[4, 2, -5, 3, 2]`.  
The prefix sums are then `[4, 6, 1, 4, 6]`, all of which are greater than `0`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    p = 0 # prefix sum
    k = 0 # prefix
    for i in a:
        p += i
        k = min(k, p)

    return 1 - k
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
[geeksforgeeks.org](https://www.geeksforgeeks.org/minimum-value-to-be-added-to-the-prefix-sums-at-each-array-indices-to-make-them-positive/)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Minimum-Initial-Value-for-Positive-Prefix-Sums)
