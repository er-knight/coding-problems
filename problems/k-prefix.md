#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)  
![](https://img.shields.io/badge/-prefix--sum-wheat) 

#### Problem :point_down:
Given an array of integers `a` and an integer `k`, return the maximum possible `i` where `a[0] + [1] + ...  + a[i] ≤ k`. Return `-1` if no valid `i` exists.
#### Sample Input :point_down:
```
a = [3, -5, 4, 1, 6]
k = 4
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
The largest `i` here is `3`, since we have `a[0] + ... + a[3] = 3` and if we added the next number `6`, the sum would no longer be less than `k`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, k):
    p = 0  # prefix sum
    j = -1 # answer
    for i, v in enumerate(a):
        p += v
        if p <= k:
            j = i

    return j
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
[binarysearch.com](https://binarysearch.com/problems/K-Prefix)
