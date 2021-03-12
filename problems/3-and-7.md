#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a positive integer `n`, determine whether you can make `n` by summing up some non-negative multiple of `3` and some non-negative multiple of `7`.
#### Sample Input :point_down:
```
n = 13
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can get `13` with `(1 * 7) + (2 * 3)`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    if (n % 3 == 0) or (n % 7 == 0):
        return True 

    while n > 0:
        n -= 3
        if n % 7 == 0:
            return True

    return False
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
def solve(n):
    if n in [3, 6, 7, 9, 10] or (n > 11):
        return True

    return False
```  
#### Hint 👇
[`Chicken Nugget Theorem`](https://brilliant.org/discussions/thread/chicken-mcnugget-theorem/) (or `Postage Stamp Problem`), states that for any two relatively prime positive integers `m`, `n`, the greatest integer that cannot be represented in the form `(a * m) + (b * n)` for non-negative integers `a`, `b` is `(m * n) − m − n)`.  
&there4; For `m = 3`, `n = 7`, the greatest integer that cannot be represented in the form `(a * 3) + (b * 7)` for non-negative integers `a`, `b` is `((3 * 7) − 3 − 7) = (21 - 3 - 7) = 11`.  
So, every integer greater than `11` can be represented in the form `(a * 3) + (b * 7)`.
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
[binarysearch.com](https://binarysearch.com/problems/3-and-7)
