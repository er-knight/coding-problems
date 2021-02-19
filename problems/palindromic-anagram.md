#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat) ![](https://img.shields.io/badge/-palindrome-wheat) ![](https://img.shields.io/badge/-anagram-wheat)

#### Problem :point_down:
Given a string `s`, determine whether any anagram of `s` is a palindrome.
#### Sample Input :point_down:
```
s = "carrace"
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`"carrace"` should return `true`, since it can be rearranged to form `"racecar"`, which is a palindrome.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    d = {}
    for i in s:
        d[i] = d.get(i, 0) + 1

    c = 0 # odd_count
    for i in d.values():
        if (i % 2 == 1):
            c += 1
        if (c > 1):
            return False

    return True
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
[binarysearch.com](https://binarysearch.com/problems/Palindromic-Anagram)  
[hackerrank.com](https://www.hackerrank.com/challenges/game-of-thrones/problem)
