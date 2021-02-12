#### Topics :point_down:
![](https://img.shields.io/badge/-hash--set-wheat)

#### Problem :point_down:
Alice has `n` candies, where the `ith` candy is of type `c[i]`. Alice noticed that she started to gain weight, so she visited a doctor.  
The doctor advised Alice to only eat `n / 2` of the candies she has (`n` is always even). Alice likes her candies very much, and she wants to eat the maximum number of different types of candies while still following the doctor's advice.  
Given the integer array `c` of length `n`, return the maximum number of different types of candies she can eat if she only eats `n / 2` of them.
#### Sample Input :point_down:
```
c = [1, 1, 2, 2, 3, 3]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
Alice can only eat `6 / 2 = 3` candies. Since there are only `3` types, she can eat one of each type.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c):
    return min(len(c)//2, len(set(c)))
```
#### Time Complexity :point_down:
```
O(n) 
```
[`list` to `set` conversion requires iterating over a list which requires `O(n)` time and adding each element to the hash set requires `O(1)` time, so the total operation is `O(n)`.](https://stackoverflow.com/questions/34642155/what-is-time-complexity-of-a-list-to-set-conversion)
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/distribute-candies/)
