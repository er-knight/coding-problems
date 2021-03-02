#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given an integer `n`, and there's `n` switches in a room all in `off` position and `n` people who flip switches as follows:
- Person `1` comes and flips all switches that are multiples of `1`, so all of them.
- Person `2` flips switches that are multiples of `2`: `2, 4, 6, ...`.
- Person `i` flips switches that are multiples of `i`.

Return number of switches that will be in `on` position at the end.
#### Sample Input :point_down:
```
n = 4
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Initially the bulbs are `[0, 0, 0, 0]`, all are `off`.
```
After player 1: [1, 1, 1, 1]
After player 2: [1, 0, 1, 0]    
After player 3: [1, 0, 0, 0]
After player 4: [1, 0, 0, 1]
```
In the end there's `2` bulbs that are `on` and `2` that are `off`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    return floor(sqrt(n))
```  
#### Hint :point_down:
```
Numbers having odd number of factors will be 'on'.
Count of numbers (≤ n) = floor(sqrt(n)).
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
[binarysearch.com](https://binarysearch.com/problems/Light-Bulb-Toggling)
