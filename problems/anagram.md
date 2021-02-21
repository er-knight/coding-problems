#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Two words are anagrams of one another if their letters can be rearranged to form the other word.  
Given a string `s`, split it into two contiguous substrings of equal length. Determine the minimum number of characters to change to make the two substrings into anagrams of one another.
#### Sample Input :point_down:
```
s = "aaabbb"
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
We split `s` into two strings `s1 = "aaa"` and `s2 = "bbb"`. We have to replace all three characters of `s1` with `"b"` to make `s1` an anagram of `s2`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    n = len(s)
    if n % 2 == 0:
        t = list(s[:n//2])
        s = s[n//2:]
        c = 0
        for i in s:
            if i in t:
                t.remove(i)
            else:
                c += 1
            
        return c
        
    return -1
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(n)
```   
#### Python :point_down:
```py
def solve(s):
    n = len(s)
    if n % 2 == 0:
        d = {}
        t = s[:n//2]
        s = s[n//2:]
        for i in range(n//2):
            d[s[i]] = d.get(s[i], 0) + 1
            d[t[i]] = d.get(t[i], 0) - 1
            
        return sum([i for i in d.values() if i > 0])
        
    return -1
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
[hackerrank.com](https://www.hackerrank.com/challenges/anagram/problem)
