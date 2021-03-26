#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
There is a new mobile game that starts with consecutively numbered clouds. Some of the clouds are thunderheads and others are cumulus. The player can jump on any cumulus cloud having a number that is equal to the number of the current cloud plus `1` or `2`. The player must avoid the thunderheads. Determine the minimum number of jumps it will take to jump from the starting postion to the last cloud. It is always possible to win the game.

For each game, you will get an array of clouds `c` numbered `0` if they are safe or `1` if they must be avoided. 
#### Sample Input :point_down:
```
c = [0, 0, 1, 0, 0, 1, 0]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
The player must avoid `c[2]` and `c[5]`. The game can be won with a minimum of `4` jumps.  

<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/clouds.png" width="300"> 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c):
    i = 0
    j = -1 # jumps
    while i < len(c):
        if (i+2) < len(c) and c[i+2] == 0:
            i += 2
        else:
            i += 1
        
        j += 1
        
    return j
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
[hackerrank.com](https://www.hackerrank.com/challenges/jumping-on-the-clouds/problem)
