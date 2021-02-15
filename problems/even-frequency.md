#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-bit--manipulation-wheat)
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Given a array of integers `a`, return whether all numbers appear an even number of times.  
This should be done in `O(1)` space.
#### Sample Input :point_down:
```
a = [2, 4, 4, 2, 3, 3]
```
#### Sample Output :point_down:
```
true
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    if (len(a) & 1):
        return False
        
    m = {} # mapping
    for i in a:
        m[i] = m.get(i, 0) + 1

    for i in m:
        if (m[i] & 1):
            return False

    return True
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```  
#### Python :point_down:
```py
def solve(a):
        if (len(a) & 1):
            return False
            
        a.sort()
        for i in range(0, len(a), 2):
            if (a[i] != a[i+1]):
                    return False

        return True
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```  
#### [@blin00](https://binarysearch.com/problems/Even-Frequency/editorials/1839347)'s Python Solution :point_down:
```py
def solve(a):
    x = 0 # xor
    for i in a:
        # constants are primes arbitrarily taken from xxhash
        h = ((i + 0x9E3779B1) * 0x85EBCA77) & 0xFFFFFFFF
        x ^= h
    return x == 0
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
[binarysearch.com](https://binarysearch.com/problems/Even-Frequency)
