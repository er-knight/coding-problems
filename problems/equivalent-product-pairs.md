#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 

#### Problem :point_down:
You are given an array of unique positive integers `a`. Return the number of quadruples (`p`, `q`, `r`, `s`) in `a`,  
such that `p * q = r * s` with `p != q != r != s`.
#### Sample Input :point_down:
```
a = [2, 3, 4, 6]
```
#### Sample Output :point_down:
```
8
```
#### Explanation :point_down:
We have the following (`p`, `q`, `r`, `s`).
```
👉 [3, 4, 2, 6]
👉 [4, 3, 2, 6]
👉 [3, 4, 6, 2]
👉 [4, 3, 6, 2]
👉 [2, 6, 3, 4]
👉 [2, 6, 4, 3]
👉 [6, 2, 3, 4]
👉 [6, 2, 4, 3]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, a):
    d = {}
    for i in range(len(a)):
        for j in range(i+1, len(a)):
            p = a[i] * a[j]
            d[p] = d.get(p, 0) + 1

    c = 0 # count
    for i in d.values():
        c += (2*i) * (2*i - 2)

    return c
```
#### Explanation :point_down:
If there are `n` pairs with product `p`, then there are `2n * (2n - 2)` quadruples where pairs in that quadruples has product `p`.
```
👉 Example 1
product = 12
pairs = [[2, 6], [3, 4]]
n = 2
quadruples = 2n * (2n - 2)
           = 4 * (4 - 2)
           = 8
---------------------------------        
👉 Example 2
product = 18
pairs = [[1, 18], [2, 9], [3, 6]]
n = 3
quadruples = 2n * (2n - 2)
           = 6 * (6 - 2)
           = 24
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Equivalent-Product-Pairs)
