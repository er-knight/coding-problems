#### Topics :point_down:
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array `h` which represents heights of `n` books, find the maximum area between 2 books after removing all the books between those 2 selected books.  
Area between any two books is calculated as `height * width`, where `height = min(h[i], h[j])` and `width = j-i-1` and `i < j` and `h[i]` and `h[j]` is height of `ith` and `jth` books respectively.
#### Sample Input :point_down:
```
n = 6
h = [2, 1, 3, 4, 6, 5]
```
#### Sample Output :point_down:
```
8
```
#### Explanation :point_down:
Remove books of height `1`, `3`, `4` and `6`. 
```
height = min(h[0], h[5]) = min(2, 5) = 2`
width  = (j - i - 1) = (5 - 0 - 1) = 4`
area   = height * width = 2 * 4 = 8
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, h):
    m = 0 # max
    i = 0
    j = n-1

    while (i < j):
        if (h[i] < h[j]):
            m = max(m, (j - i - 1) * h[i])
            i += 1
            
        elif (h[j] < h[i]):
            m = max(m, (j - i - 1) * h[j])
            j -= 1

        else:
            m = max(m, (j - i - 1) * h[i])
            i += 1
            j -= 1

    return m
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
[geeksforgeeks.org](https://www.geeksforgeeks.org/maximum-water-that-can-be-stored-between-two-buildings/)
