#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
You’re given a string `s` containing letters of three types, `R`, `B`, and `.`.  
`R` represents your current position, `B` represents a blocked position, and `.` represents an empty position. In one step, you can move to any adjacent position to your current position, as long as it is empty. Can you reach either the leftmost position or the rightmost position?  
Return `true` if you can reach either the leftmost or the rightmost position, or `false` if you cannot.
#### Sample Input :point_down:
```
s = "......B....R.............."
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can reach the rightmost position since it's not blocked.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    l = False # blocked from left
    r = False # blcoked from right
    i = 0
    while s[i] != 'R' and i < len(s):
        if s[i] == 'B':
            l = True
        i += 1
    while i < len(s):
        if s[i] == 'B':
            r = True
            break
        i += 1

    return not(l) or not(r)
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
def solve(s):
    l, r = s.split('R')
    return 'B' not in l or 'B' not in r
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
[binarysearch.com](https://binarysearch.com/problems/Rookie-Mistake)
