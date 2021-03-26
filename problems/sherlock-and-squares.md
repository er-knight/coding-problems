#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Watson likes to challenge Sherlock's math ability. He will provide a starting `a` and ending value `b` that describe a range of integers, inclusive of the endpoints. Sherlock must determine the number of square integers within that range.  
A square integer is an integer which is the square of an integer, e.g. `1, 4, 9, 16, 25` etc. 
#### Sample Input :point_down:
```
a = 35
b = 70
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
`36`, `49` and `64` are square integers in range `a = 35` to `b = 70`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, b):
    c = int(math.sqrt(a))
    d = int(math.sqrt(b))
    return d - c + int(c * c == a)
```
#### Explanation :point_down:
`sqrt(b) - sqrt(a)` gives numbers of square integers in range `a` and `b`.
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
[hackerrank.com](https://www.hackerrank.com/challenges/sherlock-and-squares/problem)
