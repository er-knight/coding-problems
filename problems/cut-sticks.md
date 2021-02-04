#### Topics :point_down:
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
You are given a number of sticks of varying lengths. You will iteratively cut the sticks into smaller sticks, discarding the shortest pieces until there are none left. At each iteration you will determine the length of the shortest stick remaining, cut that length from each of the longer sticks and then discard all the pieces of that shortest length. When all the remaining sticks are the same length, they cannot be shortened so discard them.

Given an array `a` consisting lengths of `n` sticks, print the number of sticks that are left before each iteration until there are none left.
#### Sample Input :point_down:
```
n = 6
a = [5, 4, 4, 2, 2, 8]
```
#### Sample Output :point_down:
```
6 4 2 1
```
#### Explanation :point_down:
```
sticks-length    length-of-cut   sticks-cut
 5 4 4 2 2 8          2              6
 3 2 2 _ _ 6          2              4
 1 _ _ _ _ 4          1              2
 _ _ _ _ _ 3          3              1
 _ _ _ _ _ _        DONE           DONE
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    l = len(a)
    c = [l] # sticks cut
    a.sort()
    
    for i in range(1, l):
        if (a[i] != a[i-1]):
            c.append(l - i)
            
    return c
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/cut-the-sticks/problem)
