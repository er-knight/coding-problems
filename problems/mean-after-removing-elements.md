#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:

#### Sample Input :point_down:
```
a = [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,3]
```
#### Sample Output :point_down:
```
2.00000
```
#### Explanation :point_down:
After removing `1` (minimum value) and `3` (maximum value) from array.
```
a = [2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2]
mean = sum(a)/len(a)
     = 36/18
     = 2.0
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    m = len(a)//20         # multiple of 20
    a.sort()
    s = sum(a[m:len(a)-m]) # sum
    l = len(a) - (2 * m)   # length
    return s/l
```
#### Explanation :point_down:
- `a.length` is multiple of `20`. 
- `5 % of 20 = 1`

If `a.length = 20`, remove `1` minimum and `1` maximum elements.  
If `a.length = 40`, remove `2` minimum and `2` maximum elements.  
If `a.length = 60`, remove `3` minimum and `3` maximum elements.  
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
[leetcode.com](https://leetcode.com/problems/mean-of-array-after-removing-some-elements/)
