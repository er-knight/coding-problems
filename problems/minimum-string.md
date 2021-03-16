#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given two strings `s` and `t` of equal length only consisting of lowercase letters. Assuming that you can first rearrange `s` into any order, return the minimum number of changes needed to turn `s` into `t`.
#### Sample Input :point_down:
```
s = "ehyoe"
t = "hello"
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
We can shuffle `"ehyoe"` to be `"heyeo"` and then turn `'y'` and the 2nd `'e'` into `'l'`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    d = {}
    for i in range(len(s)):
        d[s[i]] = d.get(s[i], 0) + 1
        d[t[i]] = d.get(t[i], 0) - 1

    return sum([i for i in d.values() if i > 0])
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
[binarysearch.com](https://binarysearch.com/problems/Minimum-String)
