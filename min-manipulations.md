#### Topics :point_down:
[<img src="https://img.shields.io/badge/-string-wheat">](https://github.com/topics/string)

#### Problem :point_down:
Given two lowercase strings `s1` and `s2` of same length, find minimum number of manipulations required to make two strings anagram without deleting any character.  
If two strings contains same characters in any order then strings are called anagrams.

#### Sample Input :point_down:
```
s1 = "ddcf"
s2 = "cedk"
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Change `'d'` to `'e'` and `'f'` to `'k'` in `s1`. Hence, `2` manipulations are required to make `s1` and `s2` anagrams.
```
s1 = "deck"
s2 = "cedk"
```
Now, `"deck"` and `"cedk"` are anagrams of each other, because both `s1` and `s2` contains same characters.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s1, s2):  
    count = 0
    char_count = [0] * 26
   
    for i in range(len(s1)):  
        char_count[ord(s1[i]) - ord('a')] += 1

    for i in range(len(s2)):  
        char_count[ord(s2[i]) - ord('a')] -= 1
        if (char_count[ord(s2[i]) - ord('a')] < 0) : 
            count += 1
  
    return count
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
[geeksforgeeks.org](https://www.geeksforgeeks.org/minimum-number-of-manipulations-required-to-make-two-strings-anagram-without-deletion-of-character/)
#### Solve Here :point_down:
[geeksforgeeks.org](https://practice.geeksforgeeks.org/problems/min-manipulations-to-make-strings-anagram/0)
