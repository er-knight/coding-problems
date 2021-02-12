#### Topics :point_down:
![](https://img.shields.io/badge/-prime--factors-wheat)

#### Problem :point_down:
Given a integer `n`, determine whether `n` is an ugly number.  
Ugly numbers are `positive numbers` whose prime factors only include `2, 3, 5`.  
Note: `1` is typically treated as an ugly number.
#### Sample Input :point_down:
```
n = 12
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`12 = 2 x 2 x 3`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    while (n % 2 == 0) and n:
        n //= 2
    while (n % 3 == 0) and n:
        n //= 3
    while (n % 5 == 0) and n:
        n //= 5

    return n == 1
```   
#### C++ :point_down:
```cpp
bool solve(int n) {
    while ((n % 2 == 0) and n)
        n /= 2;
    while ((n % 3 == 0) and n)
        n /= 3;
    while ((n % 5 == 0) and n)
        n /= 5;

    return n == 1;
}
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/print-all-prime-factors-of-a-given-number/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/ugly-number/)  
[binarysearch.com](https://binarysearch.com/problems/Ugly-Number)
