#### Topics :point_down:
![](https://img.shields.io/badge/-modulus-wheat)

#### Problem :point_down:
A jail has a number of prisoners `p` and a number of candiess `c` to pass out to them. Their jailer decides the fairest way to divide the treats is to seat the prisoners around a circular table in sequentially numbered chairs. A chair number `s` will be drawn from a hat. Beginning with the prisoner in that chair, one candy will be handed to each prisoner sequentially around the table until all have been distributed.

The jailer is playing a little joke, though. The last piece of candy looks like all the others, but it tastes awful. Determine the chair number occupied by the prisoner who will receive that candy.
#### Sample Input :point_down:
```
p = 7 
c = 19 
s = 2
```
#### Sample Output :point_down:
```
6
```
#### Explanation :point_down:
There are `7` prisoners, `19` candies and they are passed out starting at chair `2`. The candies go all around twice and there are `5` more candies passed to each prisoner from chair `2` to chair `6`. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p, c, s):
    w = (s + c - 1) % n
    return w if w else n
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/save-the-prisoner/problem)
