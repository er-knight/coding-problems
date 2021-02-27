#### Topics :point_down:
![](https://img.shields.io/badge/-sorting-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s`. You should re-order the string using the following algorithm:
1. Pick the smallest character from `s` and append it to the result.
2. Pick the smallest character from `s` which is greater than the last appended character to the result and append it.
3. Repeat step 2 until you cannot pick more characters.
4. Pick the largest character from `s` and append it to the result.
5. Pick the largest character from `s` which is smaller than the last appended character to the result and append it.
6. Repeat step 5 until you cannot pick more characters.
7. Repeat the steps from 1 to 6 until you pick all characters from `s`.

In each step, If the smallest or the largest character appears more than once you can choose any occurrence and append it to the result.  
Return the result string after sorting `s` with this algorithm.  
#### Sample Input :point_down:
```
s = "aaaabbbbcccc"
```
#### Sample Output :point_down:
```
"abccbaabccba"
```
#### Explanation :point_down:
```
After steps 1, 2 and 3 of the first iteration, result = "abc"
After steps 4, 5 and 6 of the first iteration, result = "abccba"
First iteration is done. 
Now s = "aabbcc" and we go back to step 1.
After steps 1, 2 and 3 of the second iteration, result = "abccbaabc"
After steps 4, 5 and 6 of the second iteration, result = "abccbaabccba"
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    d = {}
    for i in s:
        d[i] = d.get(i, 0) + 1

    a = ''.join(sorted(d.keys()))    

    r = '' # result
    i = 0
    while i < len(s):
        for c in a:
            if d[c] > 0:
                r += c
                d[c] -= 1
                i += 1
        for c in a[::-1]:
            if d[c] > 0:
                r += c
                d[c] -= 1
                i += 1

    return r
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/increasing-decreasing-string/)
