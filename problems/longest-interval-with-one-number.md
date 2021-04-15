#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
You are given an array of unique integers `a`. Return the size of the largest inclusive interval `[start, end]` such that it contains exactly one number in `a`.
#### Sample Input :point_down:
```
a = [5, 50000, 90000]
```
#### Sample Output :point_down:
```
89994
```
#### Explanation :point_down:
Following are the intervals which contains only one number.
- `[1, 49999]` contains `5`.
- `[6, 89999]` contains `50000`.
- `[50001, 100000]` contains `90000`.

The largest interval that contains one number is `[6, 89999]` which contains `50000`.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a):
    a = [0] + sorted(a) + [100001]
    s = 0
    for i in range(1, len(a)-1):
        s = max(s, a[i+1] - 1 - a[i-1])

    return s
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
[binarysearch.com](https://binarysearch.com/problems/Longest-Interval-Containing-One-Number)
