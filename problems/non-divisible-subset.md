#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a set `s` of distinct integers, print the size of a maximal subset of `s` where the sum of any `2` numbers in that subset is not evenly divisible by `k`.
#### Sample Input :point_down:
```
s = [1, 7, 2, 4]
k = 3
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
`[1, 7, 4]` is a subset of `s` where the sum of any `2` numbers is not evenly divisible by `k = 3`.
```
1 + 7 = 8  (not divisible by 3)
1 + 4 = 5  (not divisible by 3)
7 + 4 = 11 (not divisible by 3)
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(k, s):
    c = [0 for i in range(k)] # counts of remainders
    for i in s:
        c[i % k] += 1
        
    l = min(c[0], 1) # length of subset
    for i in range(1, int(k/2)+1):
        if i != (k-i):
            l += max(c[i], c[k-i])
            
    if k % 2 == 0:
        l += 1
        
    return l
```  
#### Hint :point_down:
```py
(a + b) % k = ((a % k) + (b % k)) % k
```
`a + b` is divisible by `k` when `(a % k) + (b % k)` is divisible by k.
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Reference :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/non-divisible-subset/forum/comments/150647)
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/non-divisible-subset/problem)
