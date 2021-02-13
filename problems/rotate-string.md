#### Topics :point_down:
![](https://img.shields.io/badge/-queue-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given two strings, `A` and `B`.  
A shift on `A` consists of taking string `A` and moving the leftmost character to the rightmost position. For example, if `A = 'abcde'`, then it will be `'bcdea'` after one shift on `A`. Return `true` if and only if `A` can become `B` after some number of shifts on `A`.
#### Sample Input :point_down:
```
A = "abcde" 
B = "cdeab"
```
#### Sample Output :point_down:
```
true
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(A, B):
    if (len(A) != len(B)):
        return False
    if (not(A) and not(B)):
        return True
    q = [i for i in A]
    p = [i for i in B]   
    for i in range(len(A)):
        if (p == q):
            return True
        else:
            q.append(q.pop(0))

    return False
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
def solve(A, B):
    return (len(A) == len(B)) and (A in (B * 2))
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
[leetcode.com](https://leetcode.com/problems/rotate-string/)
