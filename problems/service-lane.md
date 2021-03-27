#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
A driver is driving on the freeway. The check engine light of his vehicle is on, and the driver wants to get service immediately. Luckily, a service lane runs parallel to the highway. It varies in width along its length.  

You will be given an array of widths `w` at points along the road (indices), and another array of the indices `c` of entry and exit points. Considering each entry and exit point pair, calculate the maximum size vehicle that can travel that segment of the service lane safely.
#### Sample Input :point_down:
```
w = [2, 3, 1, 2, 3, 2, 3, 3]
c = [
    [0, 3], 
    [4, 6], 
    [6, 7], 
    [3, 5], 
    [0, 7]
]
```
#### Sample Output :point_down:
```
[1, 2, 3, 2, 1]
```
#### Explanation :point_down:
Below is the representation of the lane:
```
   | Highway | Lane | Width

0: |         |--|       2
1: |         |---|      3
2: |         |-|        1
3: |         |--|       2
4: |         |---|      3
5: |         |--|       2
6: |         |---|      3
7: |         |---|      3
```
```
w[0 to 3] → [2, 3, 1, 2]             → maximum size of vehicle = 1
w[4 to 6] → [3, 2, 3]                → maximum size of vehicle = 2
w[6 to 7] → [3, 3]                   → maximum size of vehicle = 3
w[3 to 5] → [2, 3, 2]                → maximum size of vehicle = 2
w[0 to 7] → [2, 3, 1, 2, 3, 2, 3, 3] → maximum size of vehicle = 1
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(w, c):
    a = [] # answer
    for s, e in c:
        a.append(min(w[s:e+1]))
        
    return a
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/service-lane/problem)
