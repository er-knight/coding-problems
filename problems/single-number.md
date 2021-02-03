#### Topics :point_down:
![](https://img.shields.io/badge/-xor-wheat) ![](https://img.shields.io/badge/-hash--map-wheat)

#### Problem :point_down:
Given an array of integers `a`, every element appears twice except for one. Find that single one.  
Follow up: Could you implement a solution with a linear runtime complexity and without using extra memory?
#### Sample Input :point_down:
```
a = [4,1,2,1,2]
```
#### Sample Output :point_down:
```
4
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    for k, v in d.items():
        if (v == 1):
            return k
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
def solve(a):
    xor = 0
    for i in a:
        xor ^= i

    return xor
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```  
#### Python :point_down:
```py
def solve(a):
    return ((sum(set(a)) * 2) - sum(a))
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/find-element-appears-array-every-element-appears-twice/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/single-number/)
