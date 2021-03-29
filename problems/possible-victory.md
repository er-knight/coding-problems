#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Chef is playing in a T20 cricket match. In a match, Team A plays for 20 overs. In a single over, the team gets to play 6 times, and in each of these 6 tries, they can score a maximum of 6 runs. After Team A's 20 overs are finished, Team B similarly plays for 20 overs and tries to get a higher total score than the first team. The team with the higher total score at the end wins the match.

Chef is in Team B. Team A has already played their 20 overs, and have gotten a score of `R`. Chef's Team B has started playing, and have already scored `C` runs in the first `O` overs. In the remaining `20 − O` overs, find whether it is possible for Chef's Team B to get a score high enough to win the game. That is, can their final score be strictly larger than `R`?
#### Sample Input :point_down:
```
r = 719
o = 18
c = 648
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
In the remaining `20 − O = 2` overs, Team B gets to play `2 * 6 = 12` times, and in each try, they can get a maximum of `6` score. Which means that the maximum score that they can acheieve in these `2` overs is `12 ∗ 6 = 72`. Thus, the maximum total score that Team B can achieve is `C + 72 = 720`. `720` is strictly more than Team A's score of `719`, and hence Chef's Team B can win this match.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(r, o, c):
    b = (20 - o) * 6 # remaining balls
    if (c + b * 6) > r:
        return True
    else:
        return False
```
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
[codechef.com](https://www.codechef.com/START2C/problems/T20MCH)
