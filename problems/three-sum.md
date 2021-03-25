#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array of integers `a` and an integer `k`, determine if there are three distinct elements in `a` that add up to `k`.
#### Sample Input :point_down:
```
a = [4, 1, 1, 3]
k = 5
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
```
1 + 1 + 3 = 5
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, k):
    a.sort()
    for x in range(len(a)):
        y = 0
        z = len(a)-1
        while y < z:
            if a[x] + a[y] + a[z] == k and x not in [y, z]:
                return True
            elif a[x] + a[y] + a[z] < k:
                y += 1
            else: # a[x] + a[y] + a[z] > k
                z -= 1

    return False
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Sum-of-Three-Numbers)
