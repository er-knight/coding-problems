#### Topics :point_down:
![](https://img.shields.io/badge/-binary-wheat)

#### Problem :point_down:
Reverse bits of a given 32 bits unsigned integer.
#### Sample Input :point_down:
```
n = 43261596
```
#### Sample Output :point_down:
```
964176192
```
#### Explanation :point_down:
`43261596` is represented as `00000010100101000001111010011100` in binary, so return `964176192`. `964176192`s binary representation is `00111001011110000010100101000000`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    NO_OF_BITS = 32 
    reverse_bits = 0 
    for i in range(NO_OF_BITS):
        if (n & (1 << i)): 
           reverse_bits |= 1 << ((NO_OF_BITS - 1) - i)

    return reverse_bits
```
#### Time Complexity :point_down:
```
O(number of bits)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/write-an-efficient-c-program-to-reverse-bits-of-a-number/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/reverse-bits/)
