#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given two strings `a` and `b`, both representing an integer, add them and return it in the same string representation.
This should be implemented directly, instead of using `eval` or built-in big integers.
#### Sample Input :point_down:
```
a = "12"
b = "23"
```
#### Sample Output :point_down:
```
"35"
```
#### Explanation :point_down:
```
12 + 23 = 35
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, b):
    a = a[::-1]
    b = b[::-1]
    c = 0  # carry
    s = '' # sum
    l = len(a)
    m = len(b)
    if l == m:
        for i in range(l):
            t = int(a[i]) + int(b[i]) + c
            s += str(t%10)
            c = t//10
        if c > 0:
            s += str(c)
        return s[::-1]
    elif l < m:
        i = 0
        while i < l:
            t = int(a[i]) + int(b[i]) + c
            s += str(t%10)
            c = t//10
            i += 1
        while i < m:
            t = int(b[i]) + c
            s += str(t%10)
            c = t//10
            i += 1
        if c > 0:
            s += str(c)
        return s[::-1]
    else:
        i = 0
        while i < m:
            t = int(a[i]) + int(b[i]) + c
            s += str(t%10)
            c = t//10
            i += 1
        while i < l:
            t = int(a[i]) + c
            s += str(t%10)
            c = t//10
            i += 1
        if c > 0:
            s += str(c)
        return s[::-1]
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
[binarysearch.com](https://binarysearch.com/problems/String-Addition)
