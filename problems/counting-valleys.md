#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
An avid hiker keeps meticulous records of their hikes. During the last hike that took exactly `steps`, for every step it was noted if it was an uphill, `U`, or a downhill, `D` step. Hikes always start and end at sea level, and each step up or down represents a `1` unit change in altitude. We define the following terms:  
- A mountain is a sequence of consecutive steps above sea level, starting with a step up from sea level and ending with a step down to sea level.  
- A valley is a sequence of consecutive steps below sea level, starting with a step down from sea level and ending with a step up to sea level.  

Given the sequence of up and down steps during a hike, find and print the number of valleys walked through. 
#### Sample Input :point_down:
```
steps = 8
path = UDDDUDUU
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:

If we represent `_` as sea level, a step up as `/`, and a step down as `\`, the hike can be drawn as: 

<img src="https://github.com/menobleknight/octo-adventure/blob/main/assets/valley.png" height="80">  

The hiker enters and leaves one valley.

<details>
<summary>Expand</summary>

#### Python
```py
def solve(steps, path):
    valleys = 0
    level = 0
    for i in range(steps):
        if path[i] == 'U':
            level += 1
        elif path[i] == 'D':
            level -= 1
        if (level == 0) and path[i] == 'U':
            valleys += 1
    return valleys
```
#### Time Complexity
```
O(steps)
```
#### Space Complexity
```
O(1)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/counting-valleys/problem)
