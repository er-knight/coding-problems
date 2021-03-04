#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-cycle--sort-wheat) 

#### Problem :point_down:
Given a string `s` and an integer array of indices `k` of the same length. The string `s` will be shuffled such that the character at the `ith` position moves to `k[i]` in the shuffled string. Return the shuffled string.
#### Sample Input :point_down:
```
s = "codeleet"
k = [4,5,6,7,0,2,1,3]
```
#### Sample Output :point_down:
```
"leetcode"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, k):
    t = ['' for i in range(len(s))]
    for i in range(len(s)):
        t[k[i]] = s[i]

    return ''.join(t)
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/shuffle-string/)
