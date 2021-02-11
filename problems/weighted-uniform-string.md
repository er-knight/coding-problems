#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`, let `w` be the set of weights for all possible uniform contiguous substrings of string `s`. There will be an array of queries `q` to answer where each query consists of a single integer. Create an output array `o` where for each `q[i]`, the value is `"Yes"` if `q[i]` in `w`. Otherwise, `"No"`.  
A uniform string consists of a single character repeated zero or more times. For example, `"ccc"` and `"a"` are uniform strings, but `"bcb"` and `"cd"` are not.  
The weight of a string is the sum of the weights of its characters. For example,
```
"apple" = 1 + 16 + 16 + 12 + 5 = 50
```
#### Sample Input :point_down:
```
s = "abccddde"
q = [1, 3, 12, 5, 9, 10]
```
#### Sample Output :point_down:
```
Yes Yes Yes Yes No No
```
#### Explanation :point_down:
| substring |  `w` (weights)   |
| :-------: | :--------------: |
|    `a`    |        `1`       |
|    `b`    |        `2`       |
|    `c`    |        `3`       |
|   `cc`    |   `3 + 3 = 6`    |
|    `d`    |        `4`       |
|   `dd`    |   `4 + 4 = 8`    |
|   `ddd`   | `4 + 4 + 4 = 12` |
|    `e`    |        `5`       |

```
q[0] = 1      in w, o[0] = "Yes"
q[0] = 3      in w, o[0] = "Yes"
q[0] = 12     in w, o[0] = "Yes"
q[0] = 5      in w, o[0] = "Yes"
q[0] = 9  not in w, o[0] = "No"
q[0] = 10 not in w, o[0] = "No"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, q):
    w = set() # weights
    c = 1     # counter
    for i in range(len(s)):
        t = ord(s[i]) - 96
        if (i+1 < len(s) and s[i+1] == s[i]):
            c += 1
        else:
            c = 1
        w.add(t * c)
        
    o = [] # output
    for k in q:
        if (k in w):
            o.append("Yes")
        else:
            o.append("No")
        
    return o
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
[hackerrank.com](https://www.hackerrank.com/challenges/weighted-uniform-string/problem)
