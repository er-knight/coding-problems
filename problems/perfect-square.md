#### Topics :point_down:
![](https://img.shields.io/badge/-binary--search-wheat)

#### Problem :point_down:
Given a positive integer `n`, write a function which returns `true` if `n` is a perfect square else `false`.  
Follow up: Do not use any built-in library function such as `sqrt`.
#### Sample Input :point_down:
```
n = 16
```
#### Sample Output :point_down:
```
true
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    s = 1 # start  
    e = n # end
    while (s <= e):
        m = (s + e)//2 # mid
        if (m * m == n):
            return True
        elif (m * m < n):
            s = m + 1
        else:
            e = m - 1

    return False
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```

#### Python :point_down:
```py
def solve(n):
    k = int(sqrt(n))
    return (k * k) == n
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/check-if-a-number-is-perfect-square-without-finding-square-root/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/valid-perfect-square/)
