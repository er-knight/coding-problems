#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Given an array `a` consisting of `2n` elements in the form `[x1, x2,..., xn, y1, y2,..., yn]`.  
Return the array in the form `[x1, y1, x2, y2 ,..., xn, yn]`.
#### Sample Input :point_down:
```
a = [2, 5, 1, 3, 4, 7]
n = 4
```
#### Sample Output :point_down:
```
[2, 3, 5, 4, 1, 7] 
```
#### Explanation :point_down:
```
x1 = 2 
x2 = 5 
x3 = 1 
------
y1 = 3 
y2 = 4  
y3 = 7 
```
&there4; answer is `[2, 3, 5, 4, 1, 7]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def shuffle(a, n):
    b = []
    for i in range(n):
        b.append(a[i])
        b.append(a[n+i])

    return b
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
def shuffle(a, n):
    f = lambda i: (i * 2) if i < n else ((i-n) * 2 + 1)
    for i in range(len(a)):
        j = i
        while a[i] >= 0:
            j = f(j)
            a[i], a[j] = a[j], -a[i]

    for i in range(len(a)):
        a[i] =- a[i]

    return a
```
#### Time Complexity :point_down:
```
O(n ^ 2)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[leetcode.com](https://leetcode.com/problems/shuffle-the-array/discuss/675007/Python-O(n)-time-O(1)-space-detailed-explanation)

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/shuffle-the-array/)
