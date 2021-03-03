#### Topics :point_down:
![](https://img.shields.io/badge/-greedy-wheat)
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given `n` full water bottles, you can exchange `e` empty water bottles for one full water bottle.  
The operation of drinking a full water bottle turns it into an empty bottle. Return the maximum number of water bottles you can drink.
#### Sample Input :point_down:
```
n = 15
e = 4
```
#### Sample Output :point_down:
```
19
```
#### Explanation :point_down:
You can exchange `4` empty bottles to get `1` full water bottle.  
Number of water bottles you can drink: `15 + 3 + 1 = 19`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, e):
    b = n # bottles
    while (n >= e):
        b = b + (n//e)
        n = (n//e) + (n % e)

    return b
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
[leetcode.com](https://leetcode.com/problems/water-bottles/)  
[binarysearch.com](https://binarysearch.com/problems/Beer-Bottles)
