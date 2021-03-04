#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given an integer `n`, add a dot (`"."`) as the thousands separator and return it in string format.
#### Sample Input :point_down:
```
n = 123456789
```
#### Sample Output :point_down:
```
"123.456.789"
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    n = str(n)[::-1]
    s = ''
    for i in range(0, len(n), 3):
        s += n[i:i+3]
        s += '.'
    return s[::-1][1:]
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
def solve(n):
    s = ''
    c = 0
    while n:
        if c == 3:
            s += '.'
            c = 0
        s += str(n % 10)
        c += 1
        n //= 10

    return s[::-1] if s else '0'
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
[leetcode.com](https://leetcode.com/problems/thousand-separator/)
