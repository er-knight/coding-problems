#### Topics :point_down: 
![](https://img.shields.io/badge/-hash--set-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
A pangram is a string that contains every letter of the alphabet. Given a sentence `s`, determine whether it is a pangram in the English alphabet.  
#### Sample Input :point_down:
```
s = "We promptly judged antique ivory buckles for the next prize"
```
#### Sample Output :point_down:
```
true
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def pangrams(s):
    return len(set([i for i in s.lower() if i != ' '])) == 26
```  
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/pangrams/problem)
