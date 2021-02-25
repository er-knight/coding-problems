#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
You are given an `r x c` binary matrix `m` of `1`'s (representing soldiers) and `0`'s (representing civilians). The soldiers are positioned in front of the civilians. That is, all the `1`'s will appear to the left of all the `0`'s in each row.

A row `i` is weaker than a row `j` if one of the following is true:
- The number of soldiers in row `i` is less than the number of soldiers in row `j`.
- Both rows have the same number of soldiers and `i < j`.

Return the indices of the `k` weakest rows in the matrix ordered from weakest to strongest.
#### Sample Input :point_down:
```
m = [
    [1, 1, 0, 0, 0],
    [1, 1, 1, 1, 0],
    [1, 0, 0, 0, 0],
    [1, 1, 0, 0, 0],
    [1, 1, 1, 1, 1]
] 
k = 3
```
#### Sample Output :point_down:
```
[2, 0, 3]
```
#### Explanation :point_down:
The number of soldiers in each row is: 
```
- Row 0: 2 
- Row 1: 4 
- Row 2: 1 
- Row 3: 2 
- Row 4: 5 
```
The rows ordered from weakest to strongest are `[2, 0, 3, 1, 4]`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(m, k):
    a = []
    for i in range(len(m)):
        a.append((sum(m[i]), i))

    a.sort()
    o = [] # output
    for i in range(k):
        o.append(a[i][1])

    return o
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
o(r)
```
#### Python :point_down:
```py
def solve(m, k):
    return [t[1] for t in sorted([(sum(l), i) for i, l in enumerate(m)])][:k]
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/the-k-weakest-rows-in-a-matrix/)
