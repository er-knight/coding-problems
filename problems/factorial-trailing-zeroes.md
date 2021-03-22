#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given an integer `n`, return the number of trailing zeroes in `n!`.  
Follow up: Could you write a solution that works in logarithmic time complexity?
#### Sample Input :point_down:
```
5
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
```
5! = 5 * 4 * 3 * 2 * 1 = 120
```
There is one trailing zero in `5!`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    z = 0 # zeroes
    m = 5 # multiple of 5
    while floor(n//m) >= 1:
        z += floor(n//m)
        m *= 5

    return z
```
#### Hint :point_down:
```
trailing 0s in n! = count of 5s in prime factors of n!
                  = floor(n/5) + floor(n/25) + floor(n/125) + ....
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/count-trailing-zeroes-factorial-number/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/factorial-trailing-zeroes/)  
[codechef.com](https://www.codechef.com/problems/FCTRL)
