#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given an array of integers `a` of size `n` and a positive integer `k`, determine the number of `(i, j)` pairs where `i < j` and `a[i] + a[j]` is divisible by `k`. 
#### Sample Input :point_down:
```
n = 6
k = 3
a = [1, 3, 2, 6, 1, 2]
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
Here are the `5` valid pairs when `k = 3`.
```
(0, 2) → a[0] + a[2] = 1 + 2 = 3
(0, 5) → a[0] + a[5] = 1 + 2 = 3
(1, 3) → a[1] + a[3] = 3 + 6 = 9
(2, 4) → a[2] + a[4] = 2 + 1 = 3
(4, 5) → a[4] + a[5] = 1 + 2 = 3
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, k, a):
    c = 0 # count
    for i in range(n):
        for j in range(i+1, n):
            if ((a[i] + a[j]) % k == 0):
                c += 1
                
    return c
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
[hackerrank.com](https://www.hackerrank.com/challenges/divisible-sum-pairs/problem)
