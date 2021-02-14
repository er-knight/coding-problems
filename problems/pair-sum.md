#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an array of positive integers `a`, return the number of valid pairs of indices `(i, j)`, with `i < j`, such that `a[i] + a[j]` is an `odd` number.
#### Sample Input :point_down:
```
a = [3, 2, 4]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
The two pairs are `3 + 2` and `3 + 4`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    e = 0 # even
    o = 0 # odd
    for i in a:
        if (i % 2 == 0):
            e += 1
        else:
            o += 1

    return e * o
```
#### Explanation :point_down:
We can make odd in two ways:
```
odd + even = odd
even + odd = odd
```
&there4; the indices doesn't matter, just a simple multiply of `even count` and `odd count` is required to get the answer.  
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
[binarysearch.com](https://binarysearch.com/problems/Pair-Sums)
