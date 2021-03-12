#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given a two-dimensional array of integers `r` (reviews) and a positive integer `t` (threshold). Each element `r[i]` contains `[x, y]` meaning item `i` had `x` number of 5-star reviews and a total of `y` reviews. All reviews are for one store.

Return the minimum number of additional 5-star reviews we need such that the percentage of 5-star reviews in the store is at least threshold. You can assume that it's possible to reach `threshold %` of 5-star reviews.
#### Sample Input :point_down:
```
r = [
    [4, 4],
    [1, 2],
    [3, 6]
]
t = 77
```
#### Sample Output :point_down:
```
6
```
#### Explanation :point_down:
So in total there were `8` 5-star reviews and a total of `12` reviews. To reach `77 %` 5-star reviews, we need `6` more 5-star reviews.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(r, t):
    c = 0 # count of 5 star reviews
    s = 0 # number of total reviews
    for i in r:
        c += i[0]
        s += i[1]

    p = (c * 100)//s
    n = 0 # required reviews
    while p < t:
        c += 1
        s += 1
        p = (c * 100)//s
        n += 1

    return n
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
[binarysearch.com](https://binarysearch.com/problems/5-Star-Review-Percentage)
