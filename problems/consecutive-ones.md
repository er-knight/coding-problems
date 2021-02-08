#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) ![](https://img.shields.io/badge/-greedy-wheat)

#### Problem :point_down:
You are given an array of integers `a` which contains at least one `1`. Return whether all the `1`s appear consecutively.
#### Sample Input :point_down:
```
a = [0, 1, 1, 1, 2, 3]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
All the `1`s appear consecutively here in the middle.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, a):
    c = a.count(1)
    i = 0
    while (a[i] != 1 and i < len(a)):
        i += 1
    c += i
    while (i < c):
        if (a[i] != 1):
            return False
        i += 1

    return True
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
[binarysearch.com](https://binarysearch.com/problems/Consecutive-Ones)
