#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)
![](https://img.shields.io/badge/-queue-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
You are given two arrays - `f[0], f[1], f[2], ..., f[n]`, which denote the times when an important event happens in the football match and similarly `c[0], c[1], c[2], ..., c[m]` for cricket. You have the remote in hand. You start out by watching the football match. But whenever an important event happens in the sport which isn't on the TV right now, you will be forced to switch to that sport's channel, and this continues, i.e., you switch channels if and only if when an important event in the other sport happens. Find the total number of times you will have to switch between the channels.
#### Sample Input :point_down:
```
n = 2
m = 2
f = [1, 3]
c = [2, 4]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
At `t = 0`, we are watching football match. At `t = 1` there is an important event in football match and since we are already watching the same channel we won't switch. At `t = 2`, there is an important event in cricket match and we switch the channel for the first time. At `t = 3`, there is an important event in football match and we switch the channel for the second time. At `t = 4`, there is an important event in cricket match and we switch the channel for the third time. So in total we switch three times.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, m, f, c):
    i, j = 0, 0
    w = 'football' # watching
    s = 1 # switch count
    while (i < n and j < m):
        if f[i] < c[j]:
            if w == 'cricket':
                s += 1
                w = 'football'
            i += 1 
        else:
            if w == 'football':
                s += 1 
                w = 'cricket'
            j += 1 
            
    return s
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

#### Reference :point_down:
[codechef.com](https://discuss.codechef.com/t/colglf5-editorial/87236)
#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/START2C/problems/COLGLF5)
