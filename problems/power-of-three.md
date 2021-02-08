#### Topics :point_down:
![](https://img.shields.io/badge/-power--of--three-wheat)

#### Problem :point_down:
Given an integer `n`, return `true` if it is a power of three. Otherwise, return `false`.
#### Sample Input :point_down:
```
n = 27
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`27 = 3 * 3 * 3`
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    if (n <= 0):
        return False

    while (n % 3 == 0):
        n //= 3

    return n == 1
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
    if (n <= 0):
        return False
    return (math.log10(n)/math.log10(3)) % 1 == 0
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

#### Reference :point_down:
[stackoverflow.com](https://stackoverflow.com/questions/1804311/how-to-check-if-an-integer-is-a-power-of-3)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/power-of-three/)
