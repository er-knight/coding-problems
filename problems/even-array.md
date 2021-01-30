#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) ![](https://img.shields.io/badge/-modulus-wheat)

#### Problem :point_down:
You are given an array `a` of length `n`, which consists of non-negative integers. Note that array indices start from zero.  
An array is called good if the parity of each index matches the parity of the element at that index. More formally, an array is good if for all `i`
`(0 ≤ i ≤ n−1)` the equality `i % 2 = a[i] % 2` holds, where `x % 2` is the remainder of dividing x by 2.
In one move, you can take any two elements of the array and swap them (these elements are not necessarily adjacent).
Find the minimum number of moves in which you can make the array `a` good, or return `-1` if it is not possible.
#### Sample Input :point_down:
```
n = 4
a = [3, 2, 7, 6]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:

In first step, swap 3 and 2.
```
a = [2, 3, 7, 6]
```
In second step, swap 7 and 6.
```
a = [2, 3, 6, 7]
```
Now equality `i % 2 = a[i] % 2` holds for all indices. 

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, a):
    even = 0 
    odd = 0

    for i in range(n):
        if not(i % 2 == a[i] % 2):
            if (a[i] % 2 == 1):
                odd += 1
            else:
                even += 1

    if (even == odd):
        return even
    
    return -1
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
[codeforces.com](https://codeforces.com/problemset/problem/1367/B)
