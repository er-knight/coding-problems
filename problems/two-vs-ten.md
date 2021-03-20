#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Chef Two and Chef Ten are playing a game with a number `x`. In one turn, they can multiply `x` by `2`. The goal of the game is to make `x` divisible by `10`.  
Help the Chefs to find the smallest number of turns necessary to win the game (it may be possible to win in zero turns) or return `-1` if it is impossible.
#### Sample Input :point_down:
```
x = 25
```
#### Sample Output :point_down:
```
1
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(x):
    if x % 5 == 0:
        return 0 if (x % 10 == 0) else 1

    return -1
```
#### Hint :point_down:
It is possible to make `x` divisible by `10`, only when `x` is divisible by `5`.
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/TWOVSTEN)