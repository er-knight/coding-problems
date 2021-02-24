#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
Given a non negative integer number `n`. For every numbers `i` in the range `0 ≤ i ≤ n` calculate the number of `1`'s in their binary representation and return them as an array.
#### Sample Input :point_down:
```
n = 5
```
#### Sample Output :point_down:
```
[0, 1, 1, 2, 1, 2]
```
#### Explanation :point_down:
| number | binary | `1`'s |
| :----: | :----: | :---: |
|  `0`   | `0000` |  `0`  |
|  `1`   | `0001` |  `1`  |
|  `2`   | `0010` |  `1`  |
|  `3`   | `0011` |  `2`  |
|  `4`   | `0100` |  `1`  |
|  `5`   | `0101` |  `2`  |
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    a = [0] # answer
    for i in range(1, n+1):
        c = 0 # count
        while (i):
            i &= (i-1)
            c += 1
        a.append(c)   
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

#### Python :point_down:
```py
def solve(n):
    a = [0] * (n + 1) # answer
    for i in range(1, n+1):
        if (i % 2):
            a[i] = a[i >> 1] + 1 # or a[i - 1] + 1
        else:
            a[i] = a[i >> 1]

    return a
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

#### Reference :point_down:
[twchen.gitbook.io](https://twchen.gitbook.io/leetcode/dynamic-programming/counting-bits)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/counting-bits/)  
