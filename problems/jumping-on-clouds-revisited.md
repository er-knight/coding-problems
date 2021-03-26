#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
A child is playing a cloud hopping game. In this game, there are sequentially numbered clouds that can be thunderheads or cumulus clouds. The character must jump from cloud to cloud until it reaches the start again.  
There is an array of clouds, `c` and an energy level `e = 100`. The character starts from `c[0]` and uses `1` unit of energy to make a jump of size `k` to cloud `c[(i + k) % n]`. If it lands on a thundercloud, `c[i] = 1`, its energy `e` decreases by `2` additional units. The game ends when the character lands back on cloud `0`.

Given the values of `n`, `k` and the configuration of the clouds as an array `c`, determine the final value of `e` after the game ends.
#### Sample Input :point_down:
```
n = 8
k = 2
c = [0, 0, 1, 0, 0, 1, 1, 0]
```
#### Sample Output :point_down:
```
92
```
#### Explanation :point_down:
<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/clouds2.png" width="150">

Observe that our thunderheads are the clouds numbered `2`, `5` and `6`. The player makes the following sequence of moves.  


```
Move 1] 0 → 2 
    e = 100 - 1 - 2 = 97
Move 2] 2 → 4
    e = 97 - 1 = 96
Move 3] 4 → 6
    e = 96 - 1 - 2 = 93 
Move 4] 6 → 0
    e = 93 - 1 = 92
```
Since it reaches `0th` position again, game ends.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, c, k):
    e = 100 # energy
    i = 0
    while e > 0:
        e -= 1
        if c[i] == 1:
            e -= 2
            
        i = (i + k) % n
        if i == 0:
            return e
        
    return e
```
#### Time Complexity :point_down:
```
o(n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/jumping-on-the-clouds-revisited/problem)
