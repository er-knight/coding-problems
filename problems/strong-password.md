#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Louise joined a social networking site to stay in touch with her friends. The signup page required her to input a name and a password. However, the password must be strong. The website considers a password to be strong if it satisfies the following criteria:
- Its length is at least `6`.
- It contains at least one digit.
- It contains at least one lowercase English character.
- It contains at least one uppercase English character.
- It contains at least one special character. The special characters are: `!@#$%^&*()-+`

She typed a random string `p` of length `n` in the password field but wasn't sure if it was strong. Given the string she typed, can you find the minimum number of characters she must add to make her password strong?
#### Sample Input :point_down:
```
n = 11
p = "#HackerRank"
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
The password isn't strong, but she can make it strong by adding a single digit. 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, p):        
    a = 0 # additions
    if not any([(i in '!@#$%^&*()-+') for i in p]): 
        a += 1 # special characters
    if not any([i.isupper() for i in p]): 
        a += 1 # uppercase letters
    if not any([i.islower() for i in p]): 
        a += 1 # lowercase letters
    if not any([i.isdigit() for i in p]): 
        a += 1 # digits
    
    return max(a, (6 - n)) if n < 6 else a
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
[hackerrank.com](https://www.hackerrank.com/challenges/strong-password/problem)
