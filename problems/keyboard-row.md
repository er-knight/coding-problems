#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given an array of strings `w`, return the words that can be typed using letters of the alphabet on only one row of American keyboard like the image below.

In the American keyboard:
- the first row consists of the characters `"qwertyuiop"`,
- the second row consists of the characters `"asdfghjkl"`, and
- the third row consists of the characters `"zxcvbnm"`.

#### Sample Input :point_down:
```
w = ["Hello", "Alaska", "Dad", "Peace"]
```
#### Sample Output :point_down:
```
["Alaska", "Dad"]
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(w):
    k = ['qwertyuiop', 'asdfghjkl', 'zxcvbnm']
    o = [] # output
    for i in w:
        f = True # flag
        for j in range(1, len(i)):
            if (i[j].lower() in k[0] and i[j-1].lower() not in k[0]):
                f = False
            elif (i[j].lower() in k[1] and i[j-1].lower() not in k[1]):
                f = False
            elif (i[j].lower() in k[2] and i[j-1].lower() not in k[2]):
                f = False

        if (f):
            o.append(i)

    return o
```  
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/keyboard-row/)
