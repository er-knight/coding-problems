#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array of integers `a` and a target value `k`, determine the number of pairs of array elements that have a difference equal to the target value. 
#### Sample Input :point_down:
```
k = 1
a = [1, 2, 3, 4]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
There are three pairs that differ by `k = 1`.
```
2 - 1 = 1
3 - 2 = 1
4 - 3 = 1
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def pairs(k, a):
    a.sort()
    i, j = 0, 1
    c = 0 # count
    
    while j < len(a):
        d = a[j] - a[i]
        if (d == k):
            c += 1
            j += 1
        elif (d > k):
            i += 1
        else:
            j += 1
    
    return c
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/pairs/problem)
