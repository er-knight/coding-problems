#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are given a string `s` containing `1`s and `0`s. Return the number of substrings that contain only `1`s.
#### Sample Input :point_down:
```
s = "111001"
```
#### Sample Output :point_down:
```
7
```
#### Explanation :point_down:
Here are all the substrings containing only `1`s:
```
👉 "1"
👉 "1"
👉 "1"
👉 "1"
👉 "11"
👉 "11"
👉 "111"
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(s):
    c = 0
    t = 0
    for i in s:
        if i == '1':
            t += 1
        else:
            c += (t * (t+1))//2
            t = 0

    c += (t * (t+1))//2

    return c
```  
#### Python :point_down:
```py
def solve(s):
    return sum([(len(i) * (len(i)+1))//2 for i in s.split('0')])
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
[binarysearch.com](https://binarysearch.com/problems/Count-Substrings-With-All-1s)
