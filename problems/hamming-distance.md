#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
The Hamming distance between two integers is the number of positions at which the corresponding bits are different.  
Given two integers `x` and `y`, calculate the Hamming distance.
#### Sample Input :point_down:
```
x = 1
y = 4
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
```
1   (0 0 0 1)
4   (0 1 0 0)
       ↑   ↑
```
The above arrows point to positions where the corresponding bits are different.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(x, y):
    c = 0
    x = x ^ y
    while (x):
        x &= (x-1)
        c += 1

    return c
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
[leetcode.com](https://leetcode.com/problems/hamming-distance/)
