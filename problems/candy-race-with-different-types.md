#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-stack-wheat)

#### Problem :point_down:
You are given an array of integers `c` (candies) and are playing a game against a friend. In each round, a person can remove any two consecutive candies with the same value. Given that whoever can't pick up a candy loses and that you start first, return whether you will win.
#### Sample Input :point_down:
```
c = [4, 4, 3]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
If you pick the `4`s the other person can't pick any candies.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c):
    r = 0  # rounds
    s = [] # stack
    for i in c:
        if s and i == s[-1]:
            s.pop()
            r += 1
        else:
            s.append(i)

    if r % 2 == 0:
        return False

    return True
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
[binarysearch.com](https://binarysearch.com/problems/Candy-Race-with-Different-Types)
