#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an array of integers `a`, return whether you can split the list into 1 or more groups where:
- The size of each group is larger than or equal to 2.
- The sizes of all groups are equal.
- All the integers in each group are the same.

#### Sample Input :point_down:
```
a = [2, 3, 5, 8, 3, 2, 5, 8]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can group the numbers like so:
```
[2, 2]
[3, 3]
[5, 5]
[8, 8]
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    m = min(d.values())
    for i in d.values():
        if (i < 2):
            return False
        elif (math.gcd(i, m) < 2):
            return False

    return True
```  
#### Time Complexity :point_down:
```
O(n log n)
```
because `gcd()` takes `O(log n)` time.
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    v = list(d.values())
    g = v[0]
    for i in v:
        g = math.gcd(g, i)

    return g > 1
```  
#### Time Complexity :point_down:
```
O(n log n)
```
because `gcd()` takes `O(log n)` time.
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Group-Integers)
