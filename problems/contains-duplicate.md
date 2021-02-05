#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) ![](https://img.shields.io/badge/-hashmap-wheat)

#### Problem :point_down:
Given an array of integers `a`, find if the array contains any duplicates.
Your function should return `true` if any value appears at least twice in the array, and it should return `false` if every element is distinct.
#### Sample Input :point_down:
```
a = [1, 1, 1, 3, 3, 4, 3, 2, 4, 2]
```
#### Sample Output :point_down:
```
true
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1
        if (d[i] > 1):
            return True

    return False
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
[leetcode.com](https://leetcode.com/problems/contains-duplicate/)
