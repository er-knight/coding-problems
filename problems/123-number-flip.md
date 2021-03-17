#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given an integer `n` consisting of digits `1`, `2`, and `3` and you can flip one digit to a `3`. Return the maximum number you can make.
#### Sample Input :point_down:
```
n = 123
```
#### Sample Output :point_down:
```
323
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    n = str(n)
    for i in n:
        if i != '3':
            return int(n.replace(i, '3', 1))

    return int(n)
```  
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(log n)
```
#### Python :point_down:
```py
def solve(n):
    t = 0
    f = False
    while n:
        r = n % 10
        if r != 3:
            f = True # digit != 3 found
        t = t * 10 + r
        n //= 10

    if not f:
        return t

    n = 0
    f = True
    while t:
        r = t % 10
        if f and r != 3:
            n = n * 10 + 3
            f = False
        else:
            n = n * 10 + r
        t //= 10

    return n
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
[binarysearch.com](https://binarysearch.com/problems/123-Number-Flip)
