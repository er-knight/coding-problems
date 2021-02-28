#### Topics :point_down:
![](https://img.shields.io/badge/-stack-wheat)

#### Problem :point_down:
Given a Unix path `p`, represented as a list of strings, return its resolved version.  
In Unix, `".."` means to go to the previous directory and `"."` means to stay on the current directory. By resolving, we mean to evaluate the two symbols so that we get the final directory we're currently in.
#### Sample Input :point_down:
```
p = ["usr", "..", "usr", ".", "local", "bin", "docker"]
```
#### Sample Output :point_down:
```
["usr", "local", "bin", "docker"]
```
#### Explanation :point_down:
The input represents `/usr/../usr/./local/bin/docker` which resolves to `/usr/local/bin/docker`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(p):
    s = [] # stack
    for i in p:
        if i == '..' and s:
            s.pop()
        elif i not in ['..', '.']:
            s.append(i)

    return s
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
[binarysearch.com](https://binarysearch.com/problems/Unix-Path-Resolution)
