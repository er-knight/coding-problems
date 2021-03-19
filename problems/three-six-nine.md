#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer `n`, return an array with each number from `1` to `n`, except if it's a multiple of `3` or has a `3`, `6`, or `9` in the number, it should be the string `"clap"`.  
Return the number as a string.
#### Sample Input :point_down:
```
n = 16
```
#### Sample Output :point_down:
```
["1", "2", "clap", "4", "5", "clap", "7", "8", "clap", "10", "11", "clap", "clap", "14", "clap", "clap"]
```
#### Explanation :point_down:
- `3`, `6`, `9`, `12`, and `15` are replaced by `"clap"` since they are divisible by `3`.
- `13` is replaced since it has a `3` in the number.
- `16` is replaced since it has a `6` in the number.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    a = []
    for i in range(1, n+1):
        if (i % 3 == 0):
            a.append("clap")
        elif ("3" in str(i)):
            a.append("clap")
        elif ("6" in str(i)):
            a.append("clap")
        elif ("9" in str(i)):
            a.append("clap")
        else:
            a.append(str(i))
    return a
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
def solve(n):
    
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/3-6-9)
