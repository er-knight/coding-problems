#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-hash--map-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given a array of integers `a`, return the largest integer `k` where `k` and `-k` both exist in `a` (they can be the same integer). If there's no such integer, return `-1`.
#### Sample Input :point_down:
```
a = [-4, 1, 8, -5, 4, -8]
```
#### Sample Output :point_down:
```
8
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    a.sort()
    i = 0
    j = len(a) - 1
    while (i <= j):
        if (a[i] == (-a[j])):
            return abs(a[i])
        elif (abs(a[i]) < abs(a[j])):
            j -= 1
        else:
            i += 1

    return -1
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```   
#### Python :point_down:
```py
def solve(a):
    a = set(a)
    k = -1
    for i in a:
        if -i in a:
            k = max(k, i)

    return k
```  
#### Time Complexity :point_down:
```
O(n)
```
[`list` to `set` conversion requires iterating over a list which requires `O(n)` time and adding each element to the hash set requires `O(1)` time, so the total operation is `O(n)`](https://stackoverflow.com/questions/34642155/what-is-time-complexity-of-a-list-to-set-conversion) and [set has O(1) lookup time, because there's a hash table being used underneath.](https://stackoverflow.com/a/25294938)
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/K-and-K)
