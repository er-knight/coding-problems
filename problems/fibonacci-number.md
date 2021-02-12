#### Topics :point_down:
![](https://img.shields.io/badge/-dynamic--programming-wheat) 
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-recursion-wheat)

#### Problem :point_down:
The fibonacci numbers, commonly denoted `f(n)` form a sequence, called the fibonacci sequence, such that each number is the sum of the two preceding ones, starting from `0` and `1`. That is,
```
f(0) = 0 
f(1) = 1
f(n) = f(n-1) + f(n-2), for n > 1.
```
#### Sample Input :point_down:
```
n = 4
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
```
f(4) = f(3) + f(2) = 2 + 1 = 3
f(3) = f(2) + f(1) = 1 + 1 = 2
f(2) = f(1) + f(0) = 1 + 0 = 1
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    if (n <= 1):
        return n
        
    return fib(n-1) + fib(n-2)
```  
#### Python :point_down:
```py
def solve(n):
    f = [0, 1] # fibonacci
    for i in range(2, n+1):
        f.append(f[i-1] + f[i-2])

    return f[n]
```  
#### Python :point_down:
```py
def solve(n):
    if (n <= 1):
        return n

    a, b = 0, 1
    for i in range(2, n+1):
        a, b = b, (a + b)

    return b
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/fibonacci-number/)
