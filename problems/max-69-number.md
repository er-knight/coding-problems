#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a positive integer `n` consisting only of digits `6` and `9`.  
Return the maximum number you can get by changing at most one digit (`6` becomes `9`, and `9` becomes `6`).
#### Sample Input :point_down:
```
n = 9669
```
#### Sample Output :point_down:
```
9969
```
#### Explanation :point_down:
```
- changing first  digit results in 6669.
- changing second digit results in 9969.
- changing third  digit results in 9699.
- changing fourth digit results in 9666. 
```
The maximum number is `9969`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n): 
    n = [i for i in str(n)]
    for i in range(len(n)):
        if (n[i] == '6'):
            n[i] = '9'
            break

    return ''.join(n)
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(log n)
```
#### Python :point_down:
```py
def solve(n): 
    a = 0 # answer 
    p = 10 ** int(math.log10(n))

    while p:
        if n // p == 6:
            a += (9 * p + n % p)
            return a
        if n // p == 9:
            a += (9 * p)
        n = n % p
        p = p // 10

    return a
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/maximum-69-number/)
