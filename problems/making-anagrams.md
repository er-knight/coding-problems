#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given two strings `s` and `t`, that may not be of the same length, determine the minimum number of character deletions required to make and anagrams. Any characters can be deleted from either of the strings. 
#### Sample Input :point_down:
```
s = "cde"
t = "abc"
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
```
Remove 'd' and 'e' from "cde" to get "c".
Remove 'a' and 'b' from "abc" to get "c".
```
We had to delete `4` characters to make both strings anagrams.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    d = {}
    for i in s:
        d[i] = d.get(i, 0) + 1
    for i in t:
        d[i] = d.get(i, 0) - 1
        
    return sum([abs(i) for i in d.values()])
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
[hackerrank.com](https://www.hackerrank.com/challenges/making-anagrams/problem)
