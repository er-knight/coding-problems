#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given a binary array `a`, find the maximum number of consecutive `1`'s in this array.
#### Sample Input :point_down:
```
a = [1, 1, 0, 1, 1, 1]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
The first two digits or the last three digits are consecutive `1`'s.  
The maximum number of consecutive `1`'s is `3`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    c = 0 # count
    t = 0 # temp
    for i in a:
        if (i == 1):
            t += 1
        else:
            t = 0

        c = max(c, t)

    return c
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
[leetcode.com](https://leetcode.com/problems/max-consecutive-ones/)
