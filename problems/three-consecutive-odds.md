#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given an integer array `a`, return `true` if there are three consecutive odd numbers in the array. Otherwise, return `false`. 
#### Sample Input :point_down:
```
a = [1, 2, 34, 3, 4, 5, 7, 23, 12]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`[5, 7, 23]` are three consecutive odds.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    c = 0
    for i in a:
        if (i & 1):
            c += 1
        else:
            c = 0
        if c == 3:
            return True

    return False
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
def solve(a):
    for i in range(1, len(a)-1):
        if (a[i-1] & 1) and (a[i] & 1) and (a[i+1] & 1):
            return True

    return False
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
[leetcode.com](https://leetcode.com/problems/three-consecutive-odds/)
