#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
You are choreographing a circus show with various animals.  
For one act, you are given two kangaroos on a number line ready to jump in the positive direction (i.e, toward positive infinity).
- The first kangaroo starts at location `x` and moves at a rate of `v` meters per jump.
- The second kangaroo starts at location `y` and moves at a rate of `w` meters per jump.

You have to figure out a way to get both kangaroos at the same location at the same time as part of the show. If it is possible, return `"YES"`, otherwise return `"NO"`.
#### Sample Input :point_down:
```
x = 0 
v = 3 
y = 4 
w = 2
```
#### Sample Output :point_down:
```
YES
```
#### Explanation :point_down:
The two kangaroos jump through the following sequence of locations.
![](https://s3.amazonaws.com/hr-assets/0/1516005283-e74e76ff0c-kangaroo.png)  
From the image, it is clear that the kangaroos meet at the same location (number `12` on the number line) after same number of jumps (`4` jumps), and we print `YES`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(x, v, y, w):
    if(w < v) and ((x - y) % (w - v) == 0):
        return 'YES'
    
    return 'NO'
```  
</details>

#### Reference :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/kangaroo/forum/comments/222753)
#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/kangaroo/problem)
