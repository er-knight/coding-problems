#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Spreadsheets often use this alphabetical encoding for its columns: `"A"`, `"B"`, `"C"`, ..., `"AA"`, `"AB"`, `"AC"`, ..., `"ZZ"`, `"AAA"`, `"AAB"`, `"AAC"`, ....  
Given a column number `n`, return its alphabetical column id.
#### Sample Input :point_down:
```
n = 27
```
#### Sample Output :point_down:
```
"AA"
```
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(n):
    c = '' # column id
    while n:
        n -= 1
        r = n % 26
        n = n // 26
        c += chr(65 + r)

    return c[::-1]
```  
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/The-Accountant)
