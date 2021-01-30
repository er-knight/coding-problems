#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat) ![](https://img.shields.io/badge/-prefix--sum-wheat)

#### Problem :point_down:
Given a string `s`, consisting of uppercase and lowercase letters of english alphabet, count the number of vowels in all possible substrings of `s`.

#### Sample Input :point_down:
```
s = "baceb"
```
#### Sample Output :point_down:
```
16
```
#### Explanation :point_down:
| `substrings starting from`                             | `no. of vowels` |
|--------------------------------------------------------| :-------------: |
|`'b'` &rarr; `'baceb'`, `'bace'`, `'bac'`, `'ba'`, `'b'`|       `6`       |
|`'a'` &rarr; `'aceb'`, `'ace'`, `'ac'`, `'a'`           |       `6`       |
|`'c'` &rarr; `'ceb'`, `'ce'`, `'c'`                     |       `2`       |
|`'e'` &rarr; `'eb'`, `'e'`                              |       `2`       |
|`'b'` &rarr; `'b'`                                      |       `0`       |
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    vowels = 'aeiouAEIOU'
    vowels_count = 0
    for i in range(len(s)):
        if s[i] in vowels:
            vowels_count += ((len(s) - i) * (i + 1))

    return vowels_count
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/count-the-number-of-vowels-occurred-in-the-substrings-of-given-string/)

#### Solve Here :point_down:
[hackerearth.com](https://www.hackerearth.com/practice/basic-programming/complexity-analysis/time-and-space-complexity/practice-problems/algorithm/vowel-game-f1a1047c/)
