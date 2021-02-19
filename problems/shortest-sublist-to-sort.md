#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array of integers `a`, return the length of the shortest sublist in nums which if sorted would make nums sorted in ascending order.
#### Sample Input :point_down:
```
a = [0, 1, 4, 3, 8, 9]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Sorting the sublist `[4, 3]` would get us `[0, 1, 3, 4, 8, 9]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    b = sorted(a)

    i = 0
    while (i < len(a) and a[i] == b[i]):
        i += 1

    j = len(a) - 1
    while (j >= i and a[j] == b[j]):
        j -= 1

    return j - i + 1
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
    if not a:
        return 0

    l = a[0] # left max
    e = -1   # end
    for i in range(1, len(a)):
        if (a[i] < l):
            e = i
        l = max(l, a[i]) 

    if (e == -1):
        return 0

    r = a[-1] # right min
    s = -1    # start
    for i in range(len(a)-2, -1, -1):
        if (a[i] > r):
            s = i
        r = min(r, a[i])

    return e - s + 1
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
[binarysearch.com](https://binarysearch.com/problems/Shortest-Sublist-to-Sort)
