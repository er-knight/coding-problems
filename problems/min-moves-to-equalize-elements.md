#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a non-empty integer array `a` of size `n`, find the minimum number of moves required to make all array elements equal, where a move is incrementing `n - 1` elements by `1`.
#### Sample Input :point_down:
```
a = [1, 2, 3]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
Only three moves are needed (remember each move increments two elements).
```
[1,2,3]  =>  [2,3,3]  =>  [3,4,3]  =>  [4,4,4]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    return sum(a) - (len(a) * min(a))
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/minimum-number-increment-operations-make-array-elements-equal/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/minimum-moves-to-equal-array-elements/)
