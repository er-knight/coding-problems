#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) ![](https://img.shields.io/badge/-hashmap-wheat)

#### Problem :point_down:
Given an array `a` of size `n`, return the majority element.  
The majority element is the element that appears more than `⌊n/2⌋` times.  
You may assume that the majority element always exists in the array.
#### Sample Input :point_down:
```
a = [2,2,1,1,1,2,2]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
`2` is the majority element which occurs `4` times.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    d = {}
    for i in a:
        d[i] = d.get(i, 0) + 1

    e = 0 # element
    c = 0 # count
    for k, v in d.items():
        if (v > c):
            e = k
            c = v

    return e
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```  
#### Python (using Moore’s Voting Algorithm) :point_down:
```py
def solve(a):
    m = 0 # majority index
    c = 1 # count
    for i in range(len(a)):
        if a[i] == a[m]:
            c += 1
        else:
            c -= 1
        if (c == 0):
            m = i
            c = 1

    return a[m] 
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
[geeksforgeeks.org](https://www.geeksforgeeks.org/majority-element/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/majority-element/)
