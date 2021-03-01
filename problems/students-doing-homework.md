#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given two integer arrays start time `s` and end time `e` and given an integer query time `q`.  
The `ith` student started doing their homework at the time `s[i]` and finished it at time `e[i]`.  
Return the number of students doing their homework at time `q`.  
More formally, return the number of students where `q` lays in the interval `[s[i], e[i]]` inclusive.
#### Sample Input :point_down:
```
s = [1, 2, 3] 
e = [3, 2, 7] 
q = 4
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
We have 3 students where:
```
The 1st student started doing homework at time 1 and finished at time 3 and wasn't doing anything at time 4.
The 2nd student started doing homework at time 2 and finished at time 2 and wasn't doing anything at time 4.
The 3rd student started doing homework at time 3 and finished at time 7 and he was doing homework at time 4.
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, e, q):
    a = 0 # answer
    for i in range(len(s)):
        if s[i] <= q <= e[i]:
            a += 1

    return a
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
[leetcode.com](https://leetcode.com/problems/number-of-students-doing-homework-at-a-given-time/)
