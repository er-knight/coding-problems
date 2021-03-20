#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Chef has found two very old sheets of paper, each of which originally contained a string of lowercase Latin letters. The strings on both the sheets have equal lengths. However, since the sheets are very old, some letters have become unreadable.

Chef would like to estimate the difference between these strings. Let's assume that the first string is named `s`, and the second `t`. The unreadable symbols are specified with the question mark symbol `'?'`. The difference between the strings equals to the number of positions `i`, such that `s[i]` is not equal to `t[i]`, where `s[i]` and `t[i]` denote the symbol at the `i` the position in `s` and `t`, respectively.

Chef would like to know the minimal and the maximal difference between the two strings, if he changes all unreadable symbols to lowercase Latin letters. Now that you're fully aware of Chef's programming expertise, you might have guessed that he needs you help solving this problem as well. Go on, help him!
#### Sample Input :point_down:
```
a?c
??b
```
#### Sample Output :point_down:
```
1 3
```
#### Explanation :point_down:
You can change the question marks in the strings so that you obtain `s = "abc"` and `t = "abb"`. Then `s` and `t` will differ in one position.  
On the other hand, you can change the letters so that `s = "abc"` and `t = "bab"`. Then, the strings will differ in all three positions.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s, t):
    m = 0 # max difference
    n = 0 # min difference
    for i in range(len(s)):
        if s[i] != t[i]:
            if s[i] == '?' or t[i] == '?':
                m += 1
            else:
                m += 1
                n += 1
        else:
            if s[i] == '?' and t[i] == '?':
                m += 1
            
    return (n, m)
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
[codechef.com](https://www.codechef.com/problems/CHEFSTLT)
