#### Topics :point_down:
![](https://img.shields.io/badge/-stack-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `s` representing characters typed into an editor, with `"<-"` representing a backspace, return the current state of the editor.
#### Sample Input :point_down:
```
s = "abc<-z"
```
#### Sample Output :point_down:
```
"abz"
```
#### Explanation :point_down:
The `"c"` got deleted by the backspace.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(self, s):
    t = [] # stack
    i, n = 0, len(s)
    while i < len(s):
        if s[i:i+2] == '<-':
            if t:
                t.pop()
            i += 1
        else:
            t.append(s[i])

        i += 1

    return ''.join(t)
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
[binarysearch.com](https://binarysearch.com/problems/Text-Editor)
