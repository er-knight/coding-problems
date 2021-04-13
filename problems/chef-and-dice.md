#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Chef has `n` 6-sided [standard dice](https://en.wikipedia.org/wiki/Dice) (i.e., opposite faces of dice has sum equal to `7`). Each die has dimensions `1 × 1 × 1`.  
Since Chef is bored during the quarantine, he decides to stack dice for fun.  
First, Chef forms four vertical stacks of dice (not necessarily with the same height, empty stacks are allowed) on his table, which together make up a pile of dice with base area up to `2 × 2`.  
Among all such structures, the total visible surface area of Chef's structure must be the smallest possible.  
Then, Chef calculates the number of [pips](https://en.wikipedia.org/wiki/Pip_(counting)) on the visible faces of all dice in the structure.  
A face of a die is visible if it does not touch the table or another die.

Now, he is wondering: among all possible arrangements of dice, what is the maximum possible total number of visible pips? Since he is busy cooking, he is asking you to solve this.
#### Sample Input :point_down:
```
2
```
#### Sample Output :point_down:
```
36
```
#### Explanation :point_down:

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(n):
    b = [0, 20, 36, 51] # base values
    k = n % 4           # dice on top
    h = n // 4          # height of stack
    if h == 0:
        return b[n]
    else:
        return ((h-1) * 44 + 60 + b[k] - 4 * k)
```  
#### Time Complexity :point_down:
```
O(1)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Reference :point_down:
[youtube.com](https://youtu.be/lfyWn4wdAjc)
#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/SDICE)
