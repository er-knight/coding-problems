#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hashmap-wheat) 

#### Problem :point_down:
Given an array `a` of size `n` consisting integers where `1 ≤ a[i] ≤ n`, some elements appear twice and others appear once.  
Find all the elements of `[1, n]` inclusive that do not appear in this array.  
Could you do it without extra space and in `O(n)` runtime?
#### Sample Input :point_down:
```
a = [4, 3, 2, 7, 8, 2, 3, 1]
```
#### Sample Output :point_down:
```
5 6
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    m = {} # mapping
    for i in a:
        m[i] = 1

    o = [] # output
    for i in range(len(a)):
        if (m.get(i+1, 0) == 0):
            o.append(i+1)

    return o
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
    for i in a:
        if (a[abs(i)-1] > 0):
            a[abs(i)-1] = -a[abs(i)-1]

    o = [] # output
    for i in range(len(a)):
        if (a[i] > 0):
            o.append(i+1)

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

#### Reference :point_down:
[medium.com](https://medium.com/@saurav.agg19/find-all-numbers-disappeared-in-an-array-c6a01393909)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
