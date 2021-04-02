#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
There is a collection of rocks `r` where each rock has various minerals `m` embeded in it. Each type of mineral is designated by a lowercase letter. There may be multiple occurrences of a mineral in a rock. A mineral is called a gemstone if it occurs at least once in each of the rocks in the collection.

Given an array of minerals embedded in each of the rocks, display the number of types of gemstones in the collection.
#### Sample Input :point_down:
```
r = ["abcdde", "baccd", "eeabg"]
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Only `'a'` and `'b'` occur in every rock.
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(r):
    s = set(r[0])
    for i in range(1, len(r)):
        s &= set(r[i])
        
    return len(s)
```  
#### Python :point_down:
```py
def solve(r):
    d = {}
    for m in r:
        for i in set(m):
            d[i] = d.get(i, 0) + 1
            
    return list(d.values()).count(len(r))
``` 
#### Time Complexity :point_down:
```
O(n * k)
```
where `k` is size of set.
#### Space Complexity :point_down:
```
O(k)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/gem-stones/problem)
