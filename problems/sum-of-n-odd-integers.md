#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer `n`, return the sum of the first `n` positive odd integers.
#### Sample Input :point_down:
```
5
```
#### Sample Output :point_down:
```
25
```
#### Explanation :point_down:
The first `5` odd integers are `[1, 3, 5, 7, 9]` and its sum is `25`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, n):
    s = 0 # sum
    i = 1
    while n:
        s += i
        i += 2
        n -= 1

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
#### Python :point_down:
```py
def solve(self, n):
    return (n * (2 + (n-1) * 2))//2
```
#### Hint :point_down:
```
            n * (2*a + (n-1)*d)
sum of AP = -----------------
                    2
a = 1 and d = 2
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
[binarysearch.com](https://binarysearch.com/problems/Sum-of-First-N-Odd-Integers)
