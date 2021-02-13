#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
#### Problem :point_down:
James found a love letter that his friend Harry has written to his girlfriend. James is a prankster, so he decides to meddle with the letter. He changes all the words in the letter into palindromes.  
To do this, he follows two rules:  
1. He can only reduce the value of a letter by  `1`, i.e. he can change `'d'` to `'c'`, but he cannot change `'c'` to `'d'` or `'d'` to `'b'`.
2. The letter a may not be reduced any further.

Each reduction in the value of any letter is counted as a single operation. Find the minimum number of operations required to convert a given string into a palindrome.
For example, given the string `s = "cde"`, the following two operations are performed `"cde" → "cdd" → "cdc"`. 
#### Sample Input :point_down:
```
s = "abcd"
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
`abcd → abcc → abcb → abca → abba`
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    o = 0 # operations
    l = len(s)
    for i in range((l+1)//2):
        o += abs(ord(s[i]) - ord(s[l-i-1]))
        
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
[hackerrank.com](https://www.hackerrank.com/challenges/the-love-letter-mystery/problem)
