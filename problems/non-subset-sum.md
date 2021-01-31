#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given an array `a` of size `n` consisting positive numbers, find the smallest positive integer value `k` that can't be represented as sum of elements of any subset of the given array. 
#### Sample Input :point_down:
```
n = 6
a = [1, 10, 3, 11, 6, 15]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:

2 is the smallest integer value that can't be represented as sum of elements from the array.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, n):
    a.sort()
    k = 1
    for i in range(n):
        if (a[i] <= k):
            k += a[i]
        else:
            break

    return k
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/find-smallest-value-represented-sum-subset-given-array/)
#### Solve Here :point_down:
[geeksforgeeks.org](https://practice.geeksforgeeks.org/problems/smallest-number-subset1220/1)  
[medium.com](https://medium.com/dexters-lab/eli5-find-the-smallest-positive-integer-value-that-cannot-be-represented-as-sum-of-any-subset-of-f8ea2488184b)
