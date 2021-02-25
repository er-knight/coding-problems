#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hashmap-wheat) 

#### Problem :point_down:
Given an array of integers `a`, return whether there's two numbers such that one is a triple of another.
#### Sample Input :point_down:
```
a = [2, 3, 10, 7, 6]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`6` is a triple of `2`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    for i in a:
        if i == 0:
            if d[0] > 1:
                return True
        elif d.get(i * 3, 0):
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
[binarysearch.com](https://binarysearch.com/problems/A-Number-and-Its-Triple)

#### Similar Problems :point_down:
[leetcode.com](https://leetcode.com/problems/check-if-n-and-its-double-exist/)
