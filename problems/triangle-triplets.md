#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-binary--search-wheat)
![](https://img.shields.io/badge/-sorting-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array of non-negative integers `a`, return the total number of `3` numbers `i < j < k`, such that `a[i] + a[j] > a[k]`.
#### Sample Input :point_down:
```
a = [7, 8, 8, 9, 100]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
We can make these triangles:
- `7, 8, 8`
- `7, 8, 9`
- `7, 8, 9` (using the other `8`)
- `8, 8, 9`

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    a.sort(reverse=True)
    c = 0
    n = len(a)
    for i in range(n):
        j = i + 1
        k = n - 1
        while j < k:
            if a[i] >= a[j] + a[k]:                    
                k -= 1
            else:
                c += k - j
                j += 1

    return c
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Triangle-Triplets)
