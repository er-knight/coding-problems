#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-suffix--sum-wheat) 

#### Problem :point_down:
You are given an array of non-negative integers `a`. If there are exactly `k` numbers in `a` that are greater than or equal to `k`, return `k`. Otherwise, return `-1`.
#### Sample Input :point_down:
```
a = [5, 3, 0, 9]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
There are exactly `3` numbers that's greater than or equal to `3`: `[5, 3, 9]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    m = max(a)
    s = [0 for i in range(m+1)] # suffix sum

    for i in a:
        s[i] += 1

    if (s[m] == m):
        return m

    for i in range(m-1, -1, -1):
        s[i] += s[i+1]
        if s[i] == i:
            return i

    return -1
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/K-Numbers-Greater-Than-or-Equal-to-K)
