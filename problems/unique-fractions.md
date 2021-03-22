#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given a list of lists `f` (fractions) where each list contains `[numerator, denominator]`  
which represents the number `numerator / denominator`.  
Return a new list of lists such that the numbers in fractions are:
- In their most reduced terms. e.g. `8 / 6` becomes `4 / 3`.
- Any duplicate fractions that represent the same value are removed.
- Sorted in ascending order by their value.
- If the number is negative, the `-` sign should go to the `numerator` (the input also follows this).

#### Sample Input :point_down:
```
f = [
    [8, 4],
    [2, 1],
    [7, 3],
    [14, 6],
    [10, 2],
    [-3, 6]
]
```
#### Sample Output :point_down:
```
[
    [-1, 2],
    [2, 1],
    [7, 3],
    [5, 1]
]
```
#### Explanation :point_down:
Once we reduce the numbers they become `[[2, 1], [2, 1], [7, 3], [7, 3], [5, 1], [-1, 2]]`. The result then comes from deduping and sorting by value.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(f):
    r = set() # result
    for i in f:
        a, b = i
        g = gcd(a, b)
        r.add((a//g, b//g))

    return sorted([list(i) for i in r], key=lambda t: t[0]/t[1])
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Unique-Fractions)
