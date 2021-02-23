#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-greedy-wheat)

#### Problem :point_down:
Starting with a `1-indexed` array `v` of zeros and a list of operations `q`, for each operation add a value `k` to each the array element between two given indices `a` and `b`, inclusive. Once all operations have been performed, return the maximum value in the array. 
#### Sample Input :point_down:
```
n = 5 
q = [
    [1, 2, 100],
    [2, 5, 100],
    [3, 4, 100]
]
```
#### Sample Output :point_down:
```
200
```
#### Explanation :point_down:
```
index   1    2    3    4    5
  v = [  0,   0,   0,   0,   0]
      [100, 100,   0,   0,   0]
      [100, 200, 100, 100, 100]
      [100, 200, 200, 200, 100]
```
maximum value is `200`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, q):
    v = [0 for _ in range(n+1)]
    for i in q:
        a, b, k = i
        v[a-1] += k
        v[b] -= k
            
    m = 0 # max
    c = 0 # count
    for i in v:
        c += i
        if c > m:
            m = c
            
    return m
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

#### Reference :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/crush/forum/comments/505698)
#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/crush/problem)
