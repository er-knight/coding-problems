#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-binary--search-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Let's call an array a mountain if the following properties hold
- `a.length >= 3`
- There exists some `i` with `0 < i < (a.length-1)` such that
  - `a[0] < a[1] < ... a[i-1] < a[i]`
  - `a[i] > a[i+1] > ... > a[a.length-1]`

Given an integer array `a` that is guaranteed to be a mountain, return any `i` such that  
`a[0] < a[1] < ... < a[i-1] < a[i] > a[i+1] > ... > a[arr.length-1]`.
#### Sample Input :point_down:
```
a = [0, 10, 5, 2]
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
for `i = 1`, `a[0] < a[1] > a[2]` i.e., `0 < 10 > 5 > 2`.
  
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    for i in range(1, len(a)-1):
        if (a[i-1] < a[i] > a[i+1]):
            return i
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```  
#### Python :point_down:
```py
def solve(a):
    i = 0
    j = len(a) - 1
    while (i <= j):
        m = (i + j)//2
        if (a[m-1] < a[m] > a[m+1]):
            return m
        elif (a[m-1] < a[m] < a[m+1]):
            i = m + 1
        else: # (a[m-1] > a[m] and a[m] > a[m+1])
            j = m - 1
```   
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/peak-index-in-a-mountain-array/)
