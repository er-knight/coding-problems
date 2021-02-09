#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat) ![](https://img.shields.io/badge/-stack-wheat)

#### Problem :point_down:
Given a string `s` consisting only of `"1"`s and `"0"`s, you can delete any two adjacent letters if they are different.
Return the length of the smallest string that you can make if you're able to perform this operation as many times as you want.
#### Sample Input :point_down:
```
s = "11000"
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
After deleting `"10"` we get `"100"` and we can delete another `"10"` to get `"0"` which has a length of `1`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    stack = []
    for i in s:
        if not(stack):
            stack.append(i)
        elif (i == stack[-1]):
            stack.append(i)
        else:
            stack.pop()

    return len(stack)
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```  
#### [@alexwice](https://binarysearch.com/problems/Shortest-String/editorials/430591)'s Solution:point_down:
```py
def solve(s):
    return abs(s.count('0') - s.count('1'))
```
#### Time Complexity :point_down:
```
o(n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[towardsdatascience.com](https://towardsdatascience.com/how-to-solve-python-coding-questions-using-stack-94571f31af3f)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Shortest-String)
