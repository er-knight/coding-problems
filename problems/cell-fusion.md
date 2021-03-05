#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-heap-wheat) 

#### Problem :point_down:
You are given an array of integers `c` representing sizes of different cells. In each iteration, the two largest cells `a` and `b` interact according to these rules:
- If `a = b`, they both die.
- Otherwise, the two cells merge and their size becomes `floor((a + b) / 3)`.

Return the size of the last cell or return `-1` if there's no cell is remaining.
#### Sample Input :point_down:
```
c = [10, 30, 30, 20]
```
#### Sample Output :point_down:
```
10
```
#### Explanation :point_down:
In the first iteration, the two largest cells both have the size of `30` so they both die.  
In the second iteration, cells `10`, and `20` merge to become `floor((20 + 10) / 3) = 10`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c):
    c = [-i for i in c]
    heapify(c)
    while len(c) > 1:
        a = -heappop(c)
        b = -heappop(c)
        if a != b:
            heappush(c, -floor((a+b)/3))

    return -c[0] if c else -1
```
#### Time Complexity :point_down:
```
O(n log n)
```
`O(n)` for while loop and `O(log n)` for `heappush()` and `heappop()`. 
#### Space Complexity :point_down:
```
O(n)
```
#### Reference :point_down:
[stackoverflow.com](https://stackoverflow.com/a/66423754)
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Cell-Fusion)
