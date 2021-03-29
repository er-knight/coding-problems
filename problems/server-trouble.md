#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are the Chief Engineer of a fast growing start-up. You wish to place `k` servers in some distinct locations from among `n` locations. The locations, numbered `1, 2, ..., n` are arranged in a circular manner. The distance between every adjacent location is `1` unit. `1` and `n` are adjacent.

You want to place the servers such that the maximum shortest distance between any two adjacent servers is as less as possible. Find this minimum possible distance that can be achieved, and also the minimum number of pairs of adjacent servers separated by this distance.
#### Sample Input :point_down:
```
n = 10
k = 6
```
#### Sample Output :point_down:
```
2 4
```
#### Explanation :point_down:
Let the locations be numbered from `1` to `10`. We can place the servers at locations `1, 2, 4, 6, 8 and 10`.  

<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/servers.png" width="180">  

Thus, the minimum possible maximum distance between any two adjacent servers is `2`.  
There shall be at least `4` pairs of servers separated by this distance. Here, they are `(2,4)`, `(4,6)`, `(6,8)` and `(8,10)`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, k):
    if n % k == 0:
        return (n//k, k)
    else:
        return (n//k + 1, n % k)
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
[codechef.com](https://www.codechef.com/START2C/problems/SVRT)
