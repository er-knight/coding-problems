#### Problem :point_down:
You are given a list of integers `nums`, representing the number of chess matches each person has won. Return a relative ranking (0-indexed) of each person. If two players have won the same amount, their ranking should be the same.

#### Sample Input :point_down:
```
nums = [50, 30, 50, 90, 10]
```  
#### Sample Output :point_down:
```
[1, 2, 1, 0, 3]
```
<details>
<summary>Expand</summary>

#### Python :point_down:

```python
def solve(nums):
    if not(nums):
        return nums

    temp = [(n, i) for i, n in enumerate(nums)]
    temp.sort(reverse=True, key=lambda x: x[0])

    rank = [0] * len(nums)
    rank[temp[0][1]] = 0
    r = 0

    for i in range(1, len(temp)):
        if (temp[i][0] == temp[i-1][0]):
            rank[temp[i][1]] = r
        else:
            r += 1
            rank[temp[i][1]] = r

    return rank
```

#### Time Complexity :point_down:
```
O(n log n)
```
where `n` is the length of `nums`.

#### Space Complexity :point_down:
```
O(n) 
```
where `n` is the length of `nums`.

#### [@alexwice](https://binarysearch.com/problems/Leaderboard/editorials/320867)'s Solution :point_down:
```python
def solve(nums):
    unique = sorted(set(nums), reverse=True)
    index = {v: i for i, v in enumerate(unique)}
    return [index[v] for v in nums]
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/rank-elements-array/)

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Leaderboard)
