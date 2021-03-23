#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You're given strings `j` representing the types of stones that are jewels, and `s` representing the stones you have. Each character in `s` is a type of stone you have. You want to know how many of the `stones` you have are also `jewels`.  
Letters are case sensitive, so `"a"` is considered a different type of stone from `"A"`.
#### Sample Input :point_down:
```
j = "aA"
s = "aAAbbbb"
```
#### Sample Output :point_down:
```
3
```  

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(j, s):
    m = {} # mapping
    for i in s:
        m[i] = m.get(i, 0) + 1

    c = 0 # count
    for i in j:
        c += m.get(i, 0)

    return c
```  
#### Time Complexity :point_down:
```
O(len(s))
```
#### Space Complexity :point_down:
```
O(len(s))
```  
#### Python :point_down:
```py
def solve(j, s):
    j = set(j)

    c = 0
    for i in s:
        if i in j:
            c += 1

    return c
```  
#### Time Complexity :point_down:
```
O(len(s))
```
#### Space Complexity :point_down:
```
O(len(j))
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/jewels-and-stones/)  
[codechef.com](https://www.codechef.com/problems/STONES)
