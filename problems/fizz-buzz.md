#### Topics :point_down:
![](https://img.shields.io/badge/-modulus-wheat)

#### Problem :point_down:
Write a program that outputs the string representation of numbers from `1` to `n`.  
But for multiples of three it should output `"Fizz"` instead of the number and for the multiples of five output `"Buzz"`.  
For numbers which are multiples of both three and five output `"FizzBuzz"`.
#### Sample Input :point_down:
```
n = 15
```
#### Sample Output :point_down:
```
["1", "2", "Fizz", "4", "Buzz", "Fizz", "7", "8", "Fizz", "Buzz", "11", "Fizz", "13", "14", "FizzBuzz"]
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    o = [] # output
    for i in range(1, n+1):
        if (i % 3 == 0 and i % 5 == 0):
            o.append('FizzBuzz')
        elif(i % 3 == 0):
            o.append('Fizz')
        elif (i % 5 == 0):
            o.append('Buzz')
        else:
            o.append(str(i))

    return o
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/fizz-buzz/)
