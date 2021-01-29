#### Problem
You are given a list of integers `nums`, representing the number of chess matches each person has won. Return a relative ranking (0-indexed) of each person. If two players have won the same amount, their ranking should be the same.

#### Input 
```
nums = [50, 30, 50, 90, 10]
```  
#### Output 
```
[1, 2, 1, 0, 3]
```

#### Python
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

#### Time Complexity
```
O(n log n)
```
where `n` is the length of `nums`.

#### Space Complexity
```
O(n) 
```
where `n` is the length of `nums`.

#### Reference
[geeksforgeeks.org](https://www.geeksforgeeks.org/rank-elements-array/)

#### Solve Here
[binarysearch.com](https://binarysearch.com/problems/Leaderboard)
