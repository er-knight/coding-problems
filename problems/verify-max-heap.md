#### Topics :point_down:
![](https://img.shields.io/badge/-heap-wheat) 

#### Problem :point_down:
Given an array of integers `h`, return whether it represents a `max-heap`. That is, for every `i` we have that:
- `h[i] ≥ h[2*i + 1]` if `2*i + 1` is within bounds
- `h[i] ≥ h[2*i + 2]` if `2*i + 2` is within bounds

#### Sample Input :point_down:
```
h = [4, 2, 3, 0, 1]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
```
      i = 0
(2*i)+1 = 1
(2*i)+2 = 2

h[0] ≥ h[1] and h[0] ≥ h[2]
---------------------------
      i = 1
(2*i)+1 = 3
(2*i)+2 = 4

h[1] ≥ h[3] and h[1] ≥ h[4]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(h):
    if not h:
        return True
        
    n = len(h)
    k = int(log2(n))
    for i in range(k):
        if (2*i+1) < n and h[i] < h[2*i+1]:
            return False
        if (2*i+2) < n and h[i] < h[2*i+2]:
            return False

    return True
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Verify-Max-Heap)
