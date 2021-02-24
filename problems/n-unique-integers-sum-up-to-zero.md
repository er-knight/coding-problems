#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer `n`, return any array containing `n` unique integers such that they add up to `0`.
#### Sample Input :point_down:
```
n = 5
```
#### Sample Output :point_down:
```
[-2, -1, 0, 1, 2]
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    a = []
    for i in range(1, n//2 + 1):
        a.extend([-i, i])

    if (n % 2 == 1):
        a.append(0)

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
[leetcode.com](https://leetcode.com/problems/find-n-unique-integers-sum-up-to-zero/)
