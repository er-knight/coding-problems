#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-stack-wheat)

#### Problem :point_down:
Given a target array `t` and an integer `n`. In each iteration, you will read a number from `list = {1,2,3..., n}`.  
Build the target array using the following operations:
- `Push`: Read a new element from the beginning `list`, and push it in the array.
- `Pop`: delete the last element of the array.
- If the target array is already built, stop reading more elements.

Return the operations to build the target array. You are guaranteed that the answer is unique.
#### Sample Input :point_down:
```
t = [1, 3]
n = 3
```
#### Sample Output :point_down:
```
["Push", "Push", "Pop", "Push"]
```
#### Explanation :point_down:
```
read number 1 and push in the array              → [1]
read number 2 and push in the array, then pop it → [1]
read number 3 and push in the array              → [1, 3]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(t, n):
    o = [] # output
    p = 0  # pointer
    for i in range(1, n+1):
        if p == len(t):
            return o
        elif t[p] == i:
            o.append('Push')
            p += 1
        else:
            o.extend(['Push', 'Pop'])

    return o
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
[leetcode.com](https://leetcode.com/problems/build-an-array-with-stack-operations/)
