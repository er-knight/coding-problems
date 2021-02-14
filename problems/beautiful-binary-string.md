#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Alice has a binary string. She thinks a binary string is beautiful if and only if it doesn't contain the substring `"010"`.  
In one step, Alice can change a `'0'` to a `'1'` or vice versa. Count and print the minimum number of steps needed to make Alice see the string as beautiful.  
For example, if Alice's string is `b = "010"` she can change any one element and have a beautiful string.
#### Sample Input :point_down:
```
b = "0101010"
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Change `b = "0101010"` to `b = "0111000"` in `2` steps.
```
0101010
  ↑  ↑
0111000
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(b):
    c = 0
    i = 2
    while (i < len(b)): 
        if (b[i-2:i+1] == '010'):
            c += 1 
            i += 2
        i += 1
        
    return c
```

#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```  
#### Python :point_down:
```py
def solve(b):
    return b.count('010')
```
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/beautiful-binary-string/problem)
