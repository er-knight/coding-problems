#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Little Bobby loves chocolate. He frequently goes to his favorite 5 & 10 store, Penny Auntie, to buy them. They are having a promotion at Penny Auntie. If Bobby saves enough wrappers, he can turn them in for a free chocolate.  
Given an amount of money `n` bobby has, cost of a chocolate `c` and number of wrappers he can turn in for a free chocolate `m`, return how many chocolates he can eat in total.
#### Sample Input :point_down:
```
n = 6
c = 2
m = 2
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
He spends `6` on `3` chocolates at `2` apiece. He then exchanges `2` of `3` the wrappers for additional `1` piece. Next, he uses his third leftover chocolate wrapper from his initial purchase with the wrapper from his trade-in to do a second trade-in for `1` more piece. At this point he has `1` wrapper left, which is not enough to perform another trade-in. He eats `5` chocolates.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, c, m):
    t = n//c # total chocolates
    w = t # wrappers
    while w >= m:
        t += w//m
        w = (w//m) + (w % m)
        
    return t
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
[hackerrank.com](https://www.hackerrank.com/challenges/chocolate-feast/problem)
