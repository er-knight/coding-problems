#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-heap-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given an array of strings `s` (shows), an array of integers `d` (durations), and an integer `k`, where `s[i]` and `d[i]` represent the name and duration watched by the `ith` person, return the total duration watched of the `k` most watched shows.
#### Sample Input :point_down:
```
s = ["Top Gun", "Aviator", "Top Gun", "Roma", "Logan"]
d = [5, 3, 5, 13, 4]
k = 2
```
#### Sample Output :point_down:
```
23
```
#### Explanation :point_down:
The top `k = 2` most watched movies are `"Roma"` and `"Top Gun"` for total durations of `13` and `10 = 5 + 5`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s, d, k):
    m = {}
    for i in range(len(s)):
        m[s[i]] = m.get(s[i], 0) + d[i]

    return sum(sorted(m.values(), reverse=True)[:k])
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(self, s, d, k):
    m = {}
    for i in range(len(s)):
        m[s[i]] = m.get(s[i], 0) + d[i]

    m = list([-i for i in m.values()])
    heapify(m)
    t = 0 # total duration
    for i in range(k):
        t += -heappop(m)

    return t
```
#### Time Complexity :point_down:
```
O(n) or O(k log n)
```
Because `heapify()` takes `O(n)` time, and `heappop()` takes `O(log n)` time.
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(self, s, d, k):
        m = {}
        for i in range(len(s)):
            m[s[i]] = m.get(s[i], 0) + d[i]

        m = list([i for i in m.values()])
        heapify(m)
        return sum(nlargest(k, m))
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/K-Longest-Show-Durations)
