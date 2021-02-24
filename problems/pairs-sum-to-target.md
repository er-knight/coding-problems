#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
You are given an array of integers `a` and an integer target `t`. In one operation we can remove any two numbers in `a` if the pair sums to `t`. Return the maximum number of operations we can perform.
#### Sample Input :point_down:
```
a = [1, 3, 5, 3, 7]
t = 6
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
We can pair `[1, 5]` and `[3, 3]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, t):
    a.sort()
    i = 0
    j = len(a) - 1
    c = 0 
    while (i < j):
        if (a[i] + a[j] == t):
            c += 1
            i += 1
            j -= 1
        elif (a[i] + a[j] < t):
            i += 1
        else:
            j -= 1

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
[binarysearch.com](https://binarysearch.com/problems/Sum-Pairs-to-Target)
