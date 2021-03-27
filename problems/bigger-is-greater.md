#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-permutations-wheat)

#### Problem :point_down:
[Lexicographical order](https://en.wikipedia.org/wiki/Lexicographical_order) is often known as alphabetical order when dealing with strings. A string is greater than another string if it comes later in a lexicographically sorted list.  
Given a word `w`, create a new word by swapping some or all of its characters. This new word must meet two criteria:
- It must be greater than the original word.
- It must be the smallest word that meets the first condition.

#### Sample Input :point_down:
```
abcd
```
#### Sample Output :point_down:
```
abdc
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(w):
    w = list(w)
    i = len(w)-1
    while i > 0 and w[i-1] >= w[i]:
        i -= 1
    if i <= 0:
        return 'no answer'
    
    j = len(w)-1
    while w[j] <= w[i-1]:
        j -= 1
        
    w[i-1], w[j] = w[j], w[i-1]
    
    w[i:] = w[len(w)-1:i-1:-1]
    
    return ''.join(w)
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
[nayuki.io](https://www.nayuki.io/page/next-lexicographical-permutation-algorithm)
#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/bigger-is-greater/problem)
