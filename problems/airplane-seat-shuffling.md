#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given an integer `n` representing the number of seats in an airplane. The first person has lost their ticket, so they pick a random seat. Everyone else still has their ticket, but if their seat is already taken, they will also randomly pick an available seat.

Return the probability that the last person gets their assigned seat.
#### Sample Input :point_down:
```
2
```
#### Sample Output :point_down:
```
0.5
```
#### Explanation :point_down:

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(n):
    if n == 1:
        return 1
    else:
        return 0.5
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

#### Reference :point_down:
[medium.com](https://medium.com/i-math/solving-an-advanced-probability-problem-with-virtually-no-math-5750707885f1)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Airplane-Seat-Shuffling)
