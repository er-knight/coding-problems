#### Topics :point_down: 
![](https://img.shields.io/badge/-prefix--sum-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given a binary string `s` containing `"1"`s and `"0"`s. Consider splitting the string into two non-empty substrings such that `a + b = s`. The score of this split is defined to be the sum of the number of `"0"`s in a plus the number of `"1"`s in `b`. Return the maximum score possible.
#### Sample Input :point_down:
```
s = "001001110111"
```
#### Sample Output :point_down:
```
10
```
#### Explanation :point_down:
We can split the string into `"00100" + "1110111"`. Then, thee score is `4 + 6 = 10`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    n = len(s)
    z = [0 for i in range(n)]
    z[0] = int(s[0] == '0')
    for i in range(1, n):
        z[i] = z[i-1] + (s[i] == '0')

    o = [0 for i in range(n)]
    o[-1] = int(s[-1] == '1')
    for i in range(n-2, -1, -1):
        o[i] = o[i+1] + (s[i] == '1')

    m = z[0] + o[1] # score
    for i in range(1, n-1):
        m = max(m, z[i] + o[i+1])

    return m
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(s):
    z = 0
    o = s.count('1')
    m = 0 # score
    for i in range(len(s)-1):
        if s[i] == '0':
            z += 1
        else:
            o -= 1
        m = max(m, z+o)

    return m
```
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
[binarysearch.com](https://binarysearch.com/problems/Maximize-Binary-String-Score)
