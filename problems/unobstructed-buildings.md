#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
You are given an array of integers `h` (heights) representing building heights. A building `h[i]` can see the ocean if every building on its right has shorter height.  
Return the building indices where you can see the ocean, in ascending order.
#### Sample Input :point_down:
```
a = [1, 5, 5, 2, 3]
```
#### Sample Output :point_down:
```
[2, 4]
```
#### Explanation :point_down:
We can see the ocean in building `h[2]` and `h[4]`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, h):
    a = [] # answer
    m = 0  # max height
    for i in range(len(h)-1, -1, -1):
        if h[i] > m:
            m = h[i]
            a.append(i)

    return a[::-1]
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

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Unobstructed-Buildings)
