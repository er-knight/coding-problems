#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given a sequence `a[1], a[2], ..., a[n]`.  
Find the maximum value of the expression `|a[x] − a[y]| + |a[y] − a[z]| + |a[z] − a[x]|` over all triples of pairwise distinct valid indices (`x`, `y`, `z`).
#### Sample Input :point_down:
```
a = [2, 2, 2, 2, 5]
```
#### Sample Output :point_down:
```
10
```
#### Explanation :point_down:
The value of the expression is always `10`.  
For example, let `x = 1`, `y = 2` and `z = 3`, then it is `|2 − 7| + |7 − 5| + |5 − 2| = 5 + 2 + 3 = 10`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    return 2 * (max(a) - min(a))
```
#### Explanation :point_down:
The expression `|a[x] − a[y]| + |a[y] − a[z]| + |a[z] − a[x]|` has maximum value, when `a[x] > a[y] > a[z]`.
```
∴ |a[x] − a[y]| + |a[y] − a[z]| + |a[z] − a[x]| = (a[x] − a[y]) + (a[y] − a[z]) − (a[z] − a[x])
                                                = a[x] − a[y] + a[y] − a[z] − a[z] + a[x])
                                                = a[x] − a[z] − a[z] + a[x] 
                                                = 2 * (a[x] - a[z])
                                                = 2 * (max(a) - min(a))
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
[codechef.com](https://www.codechef.com/FEB21C/problems/MAXFUN)
