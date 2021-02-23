#### Topics :point_down:
![](https://img.shields.io/badge/-stack-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s` containing brackets `(` and `)`, return the minimum number of brackets that can be inserted so that the brackets are balanced.
#### Sample Input :point_down:
```
s = ")))(("
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
We can insert `(((` to the front and `))` to the end.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s):
    t = [] # stack
    c = 0  # count
    for i in s:
        if not t:
            t.append(i)
            c += 1
        elif t[-1] == '(' and i == ')':
            t.pop()
            c -= 1
        else:
            t.append(i)
            c += 1

    return c
```  
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(self, s):
    t = [] # stack
    for i in s:
        if not t:
            t.append(i)
        elif t[-1] == '(' and i == ')':
            t.pop()
        else:
            t.append(i)

    return len(t)
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
[binarysearch.com](https://binarysearch.com/problems/Minimum-Bracket-Addition)
