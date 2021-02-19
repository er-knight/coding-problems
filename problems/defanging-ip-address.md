#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a valid (IPv4) IP address `a`, return a defanged version of that IP address.  
A defanged IP address replaces every period `"."` with `"[.]"`.

#### Sample Input :point_down:
```
a = "1.1.1.1"
```
#### Sample Output :point_down:
```
"1[.]1[.]1[.]1"
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    return a.replace('.', '[.]')
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
[leetcode.com](https://leetcode.com/problems/defanging-an-ip-address/)
