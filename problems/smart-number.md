#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
A number is called a smart number if it has an odd number of factors. Given an integer `n`, find whether it is a smart number or not.
#### Sample Input :point_down:
```
n = 4
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
`4` has 3 factors, which is an odd number.
```
factors of 4 = [1, 2, 3]
```
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(n):
    s = int(math.sqrt(n))
    if n / s == s:
        return True
        
    return False
```  
#### Hint :point_down:
An integer has odd number of factors, if it is perfect square.
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/smart-number/problem)
