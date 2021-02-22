#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of distinct integers `a`, find all pairs of elements with the minimum absolute difference of any two elements.       
Return a list of pairs in ascending order(with respect to pairs), each pair `[x, y]` follows
- `x, y` are from `a`
- `x < y`
- `y - x` equals to the minimum absolute difference of any two elements in `a`

#### Sample Input :point_down:
```
a = [4, 2, 1, 3] 
```
#### Sample Output :point_down:
```
[[1, 2], [2, 3], [3, 4]]
```
#### Explanation :point_down:
The minimum absolute difference is `1`. List all pairs with difference equal to 1 in ascending order.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    a.sort()

    m = math.inf # min absolute difference
    for i in range(1, len(a)):
        m = min(m, a[i] - a[i-1])

    o = [] # output
    for i in range(1, len(a)):
        if (a[i] - a[i-1]) == m:
            o.append([a[i-1], a[i]])

    return o
``` 
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/minimum-absolute-difference/)
