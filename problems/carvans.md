#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Chef is an avid Formula 1 fan. He went to watch this year's Indian Grand Prix at New Delhi. He noticed that one segment of the circuit was a long straight road. It was impossible for a car to overtake other cars on this segment. Therefore, a car had to lower down its speed if there was a slower car in front of it.

Formally, you're given the maximum speed of `n` cars in the order they entered the long straight segment of the circuit. Each car prefers to move at its maximum speed. If that's not possible because of the front car being slow, it might have to lower its speed. It still moves at the fastest possible speed while avoiding any collisions. For the purpose of this problem, you can assume that the straight segment is infinitely long.

Count the number of cars which were moving at their maximum speed on the straight segment.
#### Sample Input :point_down:
```
n = 5
s = [4, 5, 1, 2, 3]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
`1st` car can move at its maximum speed `4`.  
`2nd` car has to lower down its speed to `4`.  
`3rd` car can move at its maximum speed `1`.  
`4th` car has to lower down its speed to `1`.  
`5th` car has to lower down its speed to `1`.  

So `s` becomes `[4, 4, 1, 1, 1]` and only `2` cars i.e., `1st` and `3rd` car has its maximum speed.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, s):
    c = 1 
    for i in range(1, n):
        if s[i] <= s[i-1]:
            c += 1 
        s[i] = min(s[i], s[i-1])
        
    return c 
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
[codechef.com](https://www.codechef.com/problems/CARVANS)
