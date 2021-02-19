#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of integers `a`, return the minimum cost of sorting the list in ascending or descending order. The cost is defined as the sum of absolute differences between any element's old and new value.
#### Sample Input :point_down:
```
a = [1, 4, 3]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
The cost to change the list to ascending order is 2:
```
→ Change 4 to 3 for a cost of 1.
→ Change 3 to 4 for a cost of 1.
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    b = sorted(a)
    i = 0 # increasing cost
    d = 0 # decreasing cost
    for n in range(len(a)):
        i += abs(b[n] - a[n])
        d += abs(b[n] - a[-(n+1)])

    return min(i, d)
```   
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Minimum-Cost-Sort)
