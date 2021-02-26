#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of integers `a`, a lucky integer is an integer which has a frequency in the array equal to its value.  
Return a lucky integer in the array. If there are multiple lucky integers return the largest of them. If there is no lucky integer return `-1`.
#### Sample Input :point_down:
```
a = [1, 2, 2, 3, 3, 3]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
`1`, `2` and `3` are all lucky numbers, return the largest of them.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    l = -1 # lucky number
    for i in d:
        l = max(l, i) if i == d[i] else l

    return l
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
def solve(a):
    a.sort()
    c = 1  # count
    l = -1 # lucky number
    for i in range(1, len(a)):
        if a[i] == a[i-1]:
            c += 1
        else:
            if c == a[i-1]:
                l = max(l, a[i-1])
            c = 1

    if c == a[-1]:
        l = max(l, a[-1])

    return l 
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/find-lucky-integer-in-an-array/)
