#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-recursion-wheat)

#### Problem :point_down:
There is a strange counter. At the first second, it displays the number `c = 3`. Each second, the number displayed by decrements by `1` until it reaches `1`. In next second, the timer resets to `2 * c` and continues counting down. Find and print the value displayed by the counter at time `t`.
#### Sample Input :point_down:
```
17
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/counter.png" width="500">

At time `t = 17`, value of counter `c` is `5`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(t):
    c = 3 # counter
    while t > c:
        t -= c
        c *= 2
        
    return (c-t+1)
```  
#### Time Complexity :point_down:
```
O(log t)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(t, c=3):
    if t > c:
        return solve(t-c, c*2)
    
    return (c-t+1)
```  
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/strange-code/problem)
