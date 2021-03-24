#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`, encrypt it according to following scheme.  
First remove spaces from `s`. Then arrange `s` into a grid, where grid has following constraint
```py
floor(sqrt(len(s))) ≤ rows ≤ columns ≤ ceil(sqrt(len(s)))
```
Then print each column of a grid seperated by space.
#### Sample Input :point_down:
```
s = "haveaniceday"
```
#### Sample Output :point_down:
```
hae and via ecy
```
#### Explanation :point_down:
```py
len(s) = 12

√12 is between 3 and 4. 

∴ rows = 3 and columns = 4

grid = [
    [h, a, v, e],
    [a, n, i, c],
    [e, d, a, y]
]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def encryption(s):
    n = len(s)
    k = math.sqrt(n)
    r = round(math.floor(k)) # rows
    c = r if r == k else r+1 # columns
    a = '' # answer
    for i in range(c):
        a += s[i::c] + ' '
        
    return a
```
#### Time Complexity :point_down:
```
O(r * c)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/encryption/problem)
