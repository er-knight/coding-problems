#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-modulus-wheat) 

#### Problem :point_down:
A self-dividing number is a number that is divisible by every digit it contains.  
For example, `128` is a self-dividing number because `128 % 1 == 0`, `128 % 2 == 0`, and `128 % 8 == 0`.  
Also, a self-dividing number is not allowed to contain the digit zero.  
Given a lower bound `l` and upper bound `r`, output a list of every possible self dividing number, including the bounds if possible. 
#### Sample Input :point_down:
```
l = 1
r = 22
```
#### Sample Output :point_down:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 12, 15, 22]
```  
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(l, r):
    o = [] # output
    for i in range(l, r+1):
        d = [int(x) for x in str(i)] # digits
        f = True # flag
        for j in d:
            if (j == 0):
                f = False
            elif (i % j != 0):
                f = False
        if (f):
            o.append(i)

    return o
```  
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/self-dividing-numbers/)
