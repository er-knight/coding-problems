#### Topics :point_down:
![](https://img.shields.io/badge/-dynamic--programming-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given lowercase alphabet strings `s`, `t` and a positive integer `n`, return the `nth` term of the sequence `a` where:
- `a[0] = s0`
- `a[1] = s1`
- `a[n] = a[n-1] + a[n-2]` if `n` is even, otherwise `a[n] = a[n-2] + a[n-1]`.

#### Sample Input :point_down:
```
s = "a"
t = "b"
n = 4
```
#### Sample Output :point_down:
```
"bbaba"
```
#### Explanation :point_down:
The sequence `a` is 
```py
["a", "b", "ba", "bba", "bbaba"]
```
And `a[4] = "bbaba"`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t, n):
    a = [s, t]
    for i in range(2, n+1):
        if (i % 2 == 0):
            a.append(a[-1] + a[-2])
        else:
            a.append(a[-2] + a[-1])

    return a[n]
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```   

#### Python :point_down:
```py
def solve(s, t, n):
    if (n == 0):
        return s

    a, b = s, t
    for i in range(2, n+1):
        if (i % 2 == 0):
            a, b = b, b + a
        else:
            a, b = b, a + b

    return b
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
[binarysearch.com](https://binarysearch.com/problems/String-Sequence)
