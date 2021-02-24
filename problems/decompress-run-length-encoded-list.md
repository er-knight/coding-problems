#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
We are given an array `a` of integers representing an array compressed with run-length encoding.  

Consider each adjacent pair of elements `[freq, val] = [a[2*i], a[2*i+1]]` (with `i >= 0`).  
For each such pair, there are `freq` elements with value `val` concatenated in a sublist.  
Concatenate all the sublists from left to right to generate the decompressed list.  

Return the decompressed list.
#### Sample Input :point_down:
```
a = [1, 2, 3, 4]
```
#### Sample Output :point_down:
```
[2, 4, 4, 4]
```
#### Explanation :point_down:
```
The first pair [1,2] means we have freq = 1 and val = 2 so we generate the array [2].
The second pair [3,4] means we have freq = 3 and val = 4 so we generate [4,4,4].
```
At the end the concatenation `[2] + [4, 4, 4]` is `[2, 4, 4, 4]`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    b = []
    for i in range(0, len(a), 2):
        f = a[i]   # frequency
        v = a[i+1] # value
        for j in range(f):
            b.append(v)

    return b
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
    return [a[i+1] for i in range(0, len(a), 2) for j in range(a[i])]
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
[leetcode.com](https://leetcode.com/problems/decompress-run-length-encoded-list/)
