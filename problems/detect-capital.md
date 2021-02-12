#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a word `w`, you need to judge whether the usage of capitals in it is right or not.  
We define the usage of capitals in a word to be right when one of the following cases holds:  
- All letters in this word are capitals, like `"USA"`.
- All letters in this word are not capitals, like `"leetcode"`.
- Only the first letter in this word is capital, like `"Google"`.

Otherwise, we define that this word doesn't use capitals in a right way. 
#### Sample Input :point_down:
```
w = "USA"
```
#### Sample Output :point_down:
```
true
```  
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(w):
    l = 0
    u = 0
    for i in w:
        if (i.isupper()):
            u += 1
        else:
            l += 1

    if (l == len(w) or u == len(w)):
        return True
    if (u == 1 and w[0].isupper()):
        return True

    return False
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
[leetcode.com](https://leetcode.com/problems/detect-capital/)
