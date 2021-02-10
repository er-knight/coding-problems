#### Topics :point_down:  
![](https://img.shields.io/badge/-array-wheat) ![](https://img.shields.io/badge/-modulus-wheat) 

#### Problem :point_down:
You are given an array `a` of size `n`, number of rotation `k` and another array `q` consisting of indices. Rotate `a` to the right `k` times and for every index `i` in `q` return `a[i]`.
#### Sample Input :point_down:
```
n = 3 
k = 2 
a = [1, 2, 3]
q = [0, 1, 2]
```
#### Sample Output :point_down:
```
2 3 1
```
#### Explanation :point_down:
- first rotation, `a = [3, 1, 2]`.
- second rotation, `a = [2, 3, 1]`. 
```
a[q[0]] = a[0] = 2
a[q[1]] = a[1] = 3
a[q[2]] = a[2] = 1
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, k, a, q):
    o = [] # output
    for i in q:
        o.append(a[(n - (k % n) + i) % n])
        
    return o
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/circular-array-rotation/problem)
