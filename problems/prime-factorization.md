#### Topics :point_down:
![](https://img.shields.io/badge/-prime--factors-wheat)

#### Problem :point_down:
You can write out a number as a product of prime numbers, which are its prime factors. The same prime factor may occur more than once.  
Given an integer `n` greater than `1`, find all of its prime factors and return them in sorted order.
#### Sample Input :point_down:
```
n = 12
```
#### Sample Output :point_down:
```
[2, 2, 3]
```
#### Explanation :point_down:
```
2 * 2 * 3 = 12
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    factors = []
    while (n % 2 == 0):
        factors.append(2)
        n //= 2

    for i in range(3, int(sqrt(n))+1, 2):   
        while (n % i == 0):   
            factors.append(i)
            n //= i; 

    if (n > 2):  
        factors.append(n) 

    return factors
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/print-all-prime-factors-of-a-given-number/)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Prime-Factorization)
