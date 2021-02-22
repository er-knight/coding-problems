#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 

#### Problem :point_down:
Given an array of integers `a`, write a function that returns `true` if and only if the number of occurrences of each value in the array is unique.
#### Sample Input :point_down:
```
a = [1, 2, 2, 1, 1, 3]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
The value 1 has 3 occurrences, 2 has 2 and 3 has 1. No two values have the same number of occurrences.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    return len(set(d.values())) == len(d.values())
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/unique-number-of-occurrences/)
