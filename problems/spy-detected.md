#### Topics :point_down:
`array` `hash-map` `math`

#### Problem :point_down:
Given an array `a` of `n` positive integers, in which all integers except one are same, print `1-based` index of integer which occurs exactly once.

#### Sample Input :point_down:
```
n = 5
a = [1, 2, 2, 2, 2]
```
#### Sample Output :point_down:
```
1
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a, n):
    m = {}
    for i, v in enumerate(a, start=1):
        m[v] = m.get(v, []) + [i]

    for i in m:
        if len(m[i]) == 1:
            return m[i][0]
```  
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a, n):
    s = sum(a)
    k = 0
    for i in range(n - 1):
        if (s - a[i]) == (a[i + 1] * (n - 1)):
            k = i + 1
            break

    if k == 0:
        return n

    return k
```  
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[codeforces.com](https://codeforces.com/problemset/problem/1512/A)
