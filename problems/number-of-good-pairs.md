#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of integers `a`. A pair `(i,j)` is called good if `a[i] == a[j]` and `i < j`.  
Return the number of good pairs.
#### Sample Input :point_down:
```
a = [1, 2, 3, 1, 1, 3]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
```
There are 4 good pairs (0,3), (0,4), (3,4), (2,5) 0-indexed.
```
<details>
<summary>Expand</summary>


#### Python :point_down:
```py
def solve(a):
    c = 0 # count
    for i in range(len(a)):
        for j in range(i+1, len(a)):
            if a[i] == a[j]:
                c += 1

    return c
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    c = 0 # count
    for i in d.values():
        c += (i * (i - 1))//2

    return c
```
#### Explanation :point_down:
If a number appears `n` times, then `(n * (n – 1)) / 2` good pairs can be made with this number.
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
[leetcode.com](https://leetcode.com/problems/number-of-good-pairs/)
