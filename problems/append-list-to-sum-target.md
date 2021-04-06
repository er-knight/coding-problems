#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-greedy-wheat)
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given an array of integers `a` and integers `k` and `t` (target). Consider an operation where we choose an integer `-k ≤ e ≤ k` and append it to `a`.
Return the minimum number of operations required such that the sum of `a` equals to target.
#### Sample Input :point_down:
```
a = [2, 1]
k = 3
t = 10
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
We can append `[3, 3, 1]` to get `[2, 1, 3, 3, 1]` for a total sum of `10`.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a, k, t):
    return ceil(abs(sum(a) - t) / k)
```  
#### Explanation :point_down:
We can choose maximum (or minimum) value in each operation until sum of array is less than (or greater than) target.  
At last, either sum becomes equal to target or difference between sum of array and target is less than (or greater than) k.  
If the difference is zero then we need to add `difference / k` copies of `k` (or `-k`).  
If the difference is non-zero then we need add `1` more value between `0 to k` (`-k to 0`).
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Append-List-to-Sum-Target)
