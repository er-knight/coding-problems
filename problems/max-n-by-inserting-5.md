#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer `n`, return the maximum number you can make by inserting `5` anywhere in the `n`.
#### Sample Input :point_down:
```
n = 923
```
#### Sample Output :point_down:
```
9523
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, n):
    n = str(n)
    a = -math.inf # answer
    for i in range(len(n)+1):
        t = n[:i] + '5' + n[i:]
        if i == 0 and n[0] == '-':
            continue
        a = max(a, int(t))
    return a
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
[binarysearch.com](https://binarysearch.com/problems/Maximum-Number-by-Inserting-Five)
