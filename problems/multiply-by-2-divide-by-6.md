#### Topics :point_down:
`math`

#### Problem :point_down:
Given an integer `n`, find the minimum number of moves needed to make `n` equal to `1`.  
In one move, multiply `n` by `2` or divide `n` by `6` (if it's divisible by `6`). If it is impossible, return `-1`.

#### Sample Input :point_down:
```
n = 54
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
- Divide `n = 54` by `6` to get `n = 9`.
- Multiply `n = 9` by `2` to get `n = 18`. 
- Divide `n = 18` by `6` to get `n = 3`.
- Multiply `n = 3` by `2` to get `n = 6`. 
- Divide `n = 6` by `6` to get `n = 1`.

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(n):
    a, b = 0, 0
  
    while n % 2 == 0:
        n = int(n / 2)
        a += 1
  
    while n % 3 == 0:
        n = int(n / 3)
        b += 1
  
    if (n > 1) or (a > b):
        return -1

    return 2 * b - a
```  
#### Time Complexity :point_down:
```
O(log(n))
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[codeforces.com](https://codeforces.com/blog/entry/79517)

#### Solve Here :point_down:
[codeforces.com](https://codeforces.com/problemset/problem/1374/B)
