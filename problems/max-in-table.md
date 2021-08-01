#### Topics :point_down:
`recursion` `math`

#### Problem :point_down:
A `n × n` matrix `a` is defined as follows:
- `a[i][1] = 1` for `1 ≤ i ≤ n`.
- `a[1][j] = 1` for `1 ≤ j ≤ n`.
- `a[i][j] = a[i - 1][j] + a[i][j - 1]` for `1 < i ≤ n` and `1 < j ≤ n`. 

Given an integer `n`, determine the maximum value in the `n × n` matrix defined by the rules above.

#### Sample Input :point_down:
```
5
```
#### Sample Output :point_down:
```
70
```
#### Explanation :point_down:
```
a = [
    [1, 1,  1,  1,  1]
    [1, 2,  3,  4,  5]
    [1, 3,  6, 10, 15]
    [1, 4, 10, 20, 35]
    [1, 5, 15, 35, 70]
]
```
```
max(a) = 70
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(r, c):
    if r == 1 or c == 1:
        return 1

    return solve(r - 1, c) + solve(r, c - 1)
```  

</details>

#### Solve Here :point_down:
[codeforces.com](https://codeforces.com/problemset/problem/509/A)
