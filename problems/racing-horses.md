#### Topics :point_down:
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
There are `n` horses in the stable. The skill of the horse `i` is represented by an integer `s[i]`. The Chef needs to pick `2` horses for the race such that the difference in their skills is minimum. This way, he would be able to host a very interesting race. Your task is to help him do this and report the minimum difference that is possible between `2` horses in the race.
#### Sample Input :point_down:
```
s = [4, 9, 1, 32, 13]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
The minimum difference can be achieved if we pick horses with skills `1` and `4` for the race. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    s.sort()
    d = float('inf') # difference
    for i in range(1, len(s)):
        d = min(d, (s[i] - s[i-1]))
        
    return d
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/HORSES)
