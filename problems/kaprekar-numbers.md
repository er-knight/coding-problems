#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
A [kaprekar number](https://en.wikipedia.org/wiki/Kaprekar_number) is a positive whole number with a special property. If you square it, then split the number into two integers and sum those integers, you have the same value you started with.

Consider a positive whole number `n` with `d` digits. We square `n` to arrive at a number that is either `2 * d` digits long or `(2 * d) - 1` digits long. Split the string representation of the square into two parts, `l` and `r`. The right hand part `r`, must be `d` digits long. The left is the remaining substring. Convert those two substrings back to integers, add them and see if you get `n`.

Given two positive integers `p` and `q` where is `p` lower than `q`, write a program to print the kaprekar numbers in the range between `p` and `q`, inclusive. If no kaprekar numbers exist in the given range, print `INVALID RANGE`. 
#### Sample Input :point_down:
```
p = 1
q = 100
```
#### Sample Output :point_down:
```
1 9 45 55 99
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p, q):
    found = False
    for i in range(p, q+1):
        s = str(i * i)
        d = int(len(s)/2)
        l = int(s[:d]) if s[:d] else 0
        r = int(s[d:]) if s[d:] else 0
        if l + r == i:
            print(i, end=' ')
            found = True
            
    if not found:
        print('INVALID RANGE')
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/kaprekar-numbers/problem)
