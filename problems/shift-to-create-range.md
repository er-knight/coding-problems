#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
You are given an array of integers `a` of length `n`. Return whether you can make an array `[1, 2, ..., n]` or `[n, n-1, ..., 1]` by shifting `a` to the right any number of times.  
For example, shifting `[1, 2, 4, 3]` right once gives us `[3, 1, 2, 4]`.
#### Sample Input :point_down:
```
a = [4, 1, 2, 3]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can make `[1, 2, 3, 4]` by shifting `a` to the right `3` times.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a):
    k = 0
    for i in range(1, len(a)):
        if a[i-1] > a[i]:
            k = i
            break

    a = a[k:] + a[:k]
    if a == sorted(a):
        return True

    k = 0
    for i in range(1, len(a)):
        if a[i-1] < a[i]:
            k = i
            break

    a = a[k:] + a[:k]
    if a == sorted(a, reverse=True):
        return True

    return False
```  
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    n = len(a)
    if n == 1:
        return True
    c, d = 0, 0
    for i in range(n):
        if (a[(i+1) % n] - a[i]) != 1:
            c += 1
        if (a[i] - a[(i+1) % n]) != 1:
            d += 1

    return c == 1 or d == 1
```  
#### Hint :point_down:
For rotated form of `[1, 2,....n]`, there will be exactly one index `i` where `(a[(i+1) % n] - a[i]) != 1`.
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
[binarysearch.com](https://binarysearch.com/problems/Shift-to-Create-Range)
