#### Topics :point_down:
![](https://img.shields.io/badge/-anagram-wheat) ![](https://img.shields.io/badge/-hashmap-wheat)
 
#### Problem :point_down:
Given two lowercase alphabet strings `a` and `b`, return the length of the longest anagram subsequence.
#### Sample Input :point_down:
```
a = "afbc"
b = "cxba"
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
- `"abc"` is a subsequence in `"afbc"`
- `"cba"` is a subsequence in `"cxba"`

And `"abc"` and `"cba"` are anagrams of each other.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, b):
    f_a = [0] * 26 # frequencies of a 
    f_b = [0] * 26 # frequencies of b
    for i in a:
        f_a[ord(i) - 97] += 1
    for i in b:
        f_b[ord(i) - 97] += 1

    c = 0 # count
    for i in range(26):
        c += min(f_a[i], f_b[i])

    return c
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/longest-common-anagram-subsequence/)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Longest-Anagram-Subsequence)
