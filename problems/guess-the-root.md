#### Topics :point_down:
![](https://img.shields.io/badge/-binary--search-wheat)
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a non-negative integer `n`, find a number `r` such that `r * r = n` and round down to the nearest integer.  
Can you implement this without using the built-in square root?
#### Sample Input :point_down:
```
n = 26
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
```
~ 5.09901951359 is the square root of 26 and rounding down gives us 5.
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):    
    s = 0 # start
    e = n # end
    while s < e:
        m = (s + e)//2
        if (m * m <= n):
            s = m + 1
        else:
            e = m
    return (s - 1)
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
[binarysearch.com](https://binarysearch.com/problems/Guess-the-Root)
