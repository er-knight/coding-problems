#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
In academia, the `h-index` is a metric used to calculate the impact of a researcher's papers. It is calculated as follows:  
A researcher has index `h` if at least `h` papers have at least `h` citations each. If there are multiple `h` satisfying this formula, the maximum is chosen.  

Given an array of paper citations `c` of a researcher's citations, calculate their `h-index`.
#### Sample Input :point_down:
```
c = [4, 3, 0, 1, 5]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
At least `3` papers have at least `3` citations each: `3`, `4`, `5`.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(self, c):
    c.sort(reverse=True)
    h = [0]
    for i, v in enumerate(c):
        if (i+1) <= v:
            h.append(i+1)

    return max(h)
```  
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
o(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/H-Index)
