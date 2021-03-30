#### Topics :point_down:
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given a string `s` and an integer `k`. Return the number of palindromes you can construct of length `k` using only letters in `s`. Letters can be used more than once.
#### Sample Input :point_down:
```
s = "ab"
k = 4
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
We can make these palindromes `["aaaa", "bbbb", "abba", "baab"]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s, k):
    n = len(set(s))
    if k % 2 == 0:
        return pow(n, k//2)
    else:
        return pow(n, k//2) * n
```
#### Explanation :point_down:
First, we need to count the number of unique letters in the given string – we can do this by constructing a `hash-set`. A valid palindrome can have either even number or odd number of characters. If it is odd number, the middle character can have `n` choices assuming there are `n` unique characters.

When `k` is even, we can have `pow(n, k/2)` possibilities. And when `k` is odd, we need to multiply this number by `n` since we have `n` choices for that position.
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
[binarysearch.com](https://binarysearch.com/problems/Palindrome-Count)
