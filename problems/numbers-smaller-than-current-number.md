#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given the array `a`, for each `a[i]` find out how many numbers in the array are smaller than it. That is, for each `a[i]` you have to count the number of valid `j`'s such that `j != i` and `a[j] < a[i]`.   
Return the answer in an array.
#### Sample Input :point_down:
```
a = [8, 1, 2, 2, 3]
```
#### Sample Output :point_down:
```
[4, 0, 1, 1, 3]
```
#### Explanation :point_down:
```
For a[0] = 8 there are 4 smaller numbers than 8 (1, 2, 2, 3). 
For a[1] = 1 there are 0 smaller number  than 1.
For a[2] = 2 there are 1 smaller number  than 2 (1). 
For a[3] = 2 there are 1 smaller number  than 2 (1). 
For a[4] = 3 there are 3 smaller numbers than 3 (1, 2, 2).
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    o = [0 for _ in range(len(a))] # output
    for i in range(len(a)):
        c = 0
        for j in range(len(a)):
            if a[j] < a[i]:
                c += 1
        o[i] = c

    return o
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a):
    d = {}
    b = sorted([i for i in a])
    for i, v in enumerate(b):
        k = d.get(v, -1)
        d[v] = i if k == -1 else min(i, k)

    o = [] # output
    for i in a:
        o.append(d[i])

    return o
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(a):
    c = [0 for _ in range(101)] # count
        
    for i in a:
        c[i] += 1
    for i in range(1, 101):
        c[i] += c[i-1]

    o = [0 for _ in range(len(a))] # output
    for i in range(len(a)):
        if a[i] == 0:
            o[i] = 0
        else:
            o[i] = c[a[i]-1]

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
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)
