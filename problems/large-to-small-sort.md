#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array of integers `a`, sort the array in the following way:
- `1st` number is the maximum.
- `2nd` number is the minimum.
- `3rd` number is the `2nd` maximum.
- `4th` number is the `2nd` minimum and so on.

#### Sample Input :point_down:
```
a = [5, 2, 9, 3]
```
#### Sample Output :point_down:
```
[9, 2, 5, 3]
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a):
    a.sort()
    b = []
    i, j = 0, len(a)-1
    f = 1 # flag
    while i <= j:
        if f == 1:
            b.append(a[j])
            j -= 1
            f = 0
        else:
            b.append(a[i])
            i += 1
            f = 1

    return b
```  
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Large-to-Small-Sort)
