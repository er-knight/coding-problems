#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)

#### Problem :point_down:
In an array of integers `a`, a triplet `(a[i], a[j], a[k])` is beautiful if:
- `i < j < k`
- `a[j] - a[i] = a[k] - a[j] = d`

Given an array of integers `a` (sorted in increasing order) and the value of `d`, count the number of beautiful triplets in array `a`.
#### Sample Input :point_down:
```
d = 3
a = [1, 2, 4, 5, 7, 8, 10]
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
There are `3` beautiful triplets:
```
👉 [1, 4, 7]
👉 [4, 7, 10]
👉 [2, 5, 8]
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def beautifulTriplets(d, a):
    s = set(a)
    c = 0
    for i in a:
        if (i+d) in s and (i+2*d) in s:
            c += 1
            
    return c
```
#### Explanation :point_down:
Let `a[i], a[j], a[k]` is an [Arithmetic Progression](https://en.wikipedia.org/wiki/Arithmetic_progression) of 3 terms.  
Then, first term is `a[i]`, second term is `a[j] = a[i] + d` and third term is `a[k] = a[i] + (2 * d)` where `d` is common difference.
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/beautiful-triplets/problem)
