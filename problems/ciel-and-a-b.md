#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
In Ciel's restaurant, a waiter is training. Since the waiter isn't good at arithmetic, sometimes he gives guests wrong change. Ciel gives him a simple problem. What is `a - b` (`a minus b`)?

Surprisingly, his answer is wrong. To be more precise, his answer has exactly one wrong digit. Can you imagine this? Can you make the same mistake in this problem? Return `a - b` with one wrong digit.
#### Sample Input :point_down:
```
a = 5858
b = 1234
```
#### Sample Output :point_down:
```
4625
```
#### Explanation :point_down:
```
5858 - 1234 = 4624
```
`4625` has only one digit different from `4624`.  
`3625`, `4725`, etc. are also valid answers.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, b):
    c = a - b
    return (c - 1) if (c % 10 == 9) else (c + 1)
```
#### Explanation :point_down:
If `(a - b) % 10 != 9`, then return `(a - b - 1)`. Only one digit is changing.  
If `(a - b) % 10 == 9` and if we return `(a - b - 1)`, then more than one digit may change.  
So, return `(a - b + 1)`, if `(a - b) % 10 == 9`.
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
[codechef.com](https://www.codechef.com/problems/CIELAB)
