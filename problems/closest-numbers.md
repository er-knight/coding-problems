
#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of unsorted integers `a`, find the pair of elements that have the smallest absolute difference between them. If there are multiple pairs, find them all.
#### Sample Input :point_down:
```
a = [5, 4, 3, 2]
```
#### Sample Output :point_down:
```
[2, 3, 3, 4, 4, 5]
```
#### Explanation :point_down:
The minimum absolute difference is `1`. Valid pairs are `2, 3`, `3, 4`, and `4, 5`. 
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a):
    m = math.inf
    a.sort()
    for i in range(1, len(a)):
        m = min(m, (a[i] - a[i-1]))
        
    b = []
    for i in range(1, len(a)):
        if (a[i] - a[i-1]) == m:
            b.append(a[i-1])
            b.append(a[i])
            
    return b
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
[hackerrank.com](https://www.hackerrank.com/challenges/closest-numbers/problem)
