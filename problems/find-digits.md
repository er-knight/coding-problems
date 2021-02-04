#### Topics :point_down:
![](https://img.shields.io/badge/-modulus-wheat)

#### Problem :point_down:
Given an integer `n`, for each digit that makes up `n` determine whether it is a divisor.  
Count the number of divisors occurring within the integer. 
#### Sample Input :point_down:
```
n = 1012
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
The number `1012` is broken into four digits, `1`, `0`, `1`, and `2`. `1012` is evenly divisible by its digits `1`, `1`, and `2`, but it is not divisible by `0` as division by zero is undefined.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    d = [int(i) for i in str(n)] # digits
    c = 0 # count
    
    for i in d:
        if (i != 0 and n % i == 0):
            c += 1
            
    return c
```
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(log n)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/find-digits/problem)
