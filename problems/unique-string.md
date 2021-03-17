#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a lowercase alphabet string `s`, determine whether it has all unique characters.
#### Sample Input :point_down:
```
s = "abcde"
```
#### Sample Output :point_down:
```
true
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    d = {}
    for i in s:
        if d.get(i, 0):
            return False
        else:
            d[i] = 1

    return True
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(s):
    t = set()
    for i in s:
        if i in t:
            return False
        else:
            t.add(i)

    return True
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(s):
    return len(set(s)) == len(s)
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
[binarysearch.com](https://binarysearch.com/problems/A-Unique-String)
