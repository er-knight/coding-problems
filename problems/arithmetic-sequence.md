#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given an array of integers `a` that used to be an arithmetic sequence. Given that a number was removed, and that the number was not the first or the last element, return the removed number.
#### Sample Input :point_down:
```
a = [1, 3, 5, 9]
```
#### Sample Output :point_down:
```
7
```  
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    n = len(a)
    d = int((a[-1] - a[0])/n)

    k = a[0]
    for i in range(1, n):
        k += d
        if (k != a[i]):
            return k 

    return a[0]
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
    n = len(a)
    k = a[0] + a[-1]
    s = sum(a)
    return int(k * (n + 1)/2) - s
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
[binarysearch.com](https://binarysearch.com/problems/Complete-an-Arithmetic-Sequence/submissions)
