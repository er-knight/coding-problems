#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given the array of paths `p`, where `p[i] = [cityA, cityB]` means there exists a direct path going from `cityA` to `cityB`. Return the destination city, that is, the city without any path outgoing to another city.  
It is guaranteed that the graph of paths forms a line without any loop, therefore, there will be exactly one destination city.
#### Sample Input :point_down:
```
p = [
    ["London", "New York"], 
    ["New York", "Lima"], 
    ["Lima", "Sao Paulo"]
]
```
#### Sample Output :point_down:
```
"Sao Paulo" 
```
#### Explanation :point_down:
Starting at `"London"` city you will reach `"Sao Paulo"` city which is the destination city. 
Your trip consist of:
```
"London" → "New York" → "Lima" → "Sao Paulo"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p):        
    m = {} # map
    for (s, d) in p:
        m[s] = d

    s = p[0][0] 
    while m.get(s):
        s = m.get(s)

    return s
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
def solve(p):        
    s = {i[0] for i in p} # sources
    d = {i[1] for i in p} # destinations

    for i in d:
        if i not in s:
            return i
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
def solve(p):     
    return list({i[1] for i in p} - {i[0] for i in p})[0]
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/destination-city/)
