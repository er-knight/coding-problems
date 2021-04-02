#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of integers `a`, sort the array such that:
- All even numbers are sorted in increasing order.
- All odd numbers are sorted in decreasing order.
- The relative positions of the even and odd numbers remain the same.

#### Sample Input :point_down:
```
a = [8, 13, 11, 90, -5, 4]
```
#### Sample Output :point_down:
```
[4, 13, 11, 8, -5, 90]
```
#### Explanation :point_down:
The even numbers are sorted in increasing order, the odd numbers are sorted in decreasing number, and the relative positions were  
`[even, odd, odd, even, odd, even]` and remain the same after sorting.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(self, a):
    o = [] # odd
    e = [] # even
    for x in a:
        if x % 2 == 0:
            e.append(x)
        else:
            o.append(x)

    o.sort()
    e.sort(reverse=True)

    for i, x in enumerate(a):
        if x % 2 == 0:
            a[i] = e.pop()
        else:
            a[i] = o.pop()

    return a
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
[binarysearch.com](https://binarysearch.com/problems/Mixed-Sorting)
