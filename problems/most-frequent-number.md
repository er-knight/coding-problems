#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given `n` integer ranges, find the maximum occurring integer in these ranges. If more than one such integer exits, find the smallest one. 
The ranges are given as two arrays `l` and `r`. `l[i]` consists of starting point of range and `r[i]` consists of corresponding end point of the range. 
#### Sample Input :point_down:
```
n = 4
l = [1, 4, 3, 1]
r = [15, 8, 5, 4]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
```
[1, 15] = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
[4, 8]  = [4, 5, 6, 7, 8]
[3, 5]  = [3, 4, 5]
[1, 4]  = [1, 2, 3, 4]
```
The maximum occurring integer in these ranges is `4`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, l, r):
    a = [0] * (max(r) + 2)

    for i in range(n): 
        a[l[i]] += 1
        a[r[i]+1] -= 1
 
    s = a[0]   # max prefix sum 
    n = 0      # max frequency value
    for i in range(1, max(r) + 2): 
        a[i] += a[i-1] 
        if (s < a[i]): 
            s = a[i] 
            n = i 
    return n
```
#### Time Complexity :point_down:
```
O(max(r))
```
#### Space Complexity :point_down:
```
O(max(r))
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/maximum-occurred-integer-n-ranges/)
#### Solve Here :point_down:
[geeksforgeeks.org](https://practice.geeksforgeeks.org/problems/maximum-occured-integer4602/1)
#### Similar Problems :point_down:
[binarysearch.com](https://binarysearch.com/problems/Most-Frequent-Number-in-Intervals)
