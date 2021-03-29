#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--set-wheat)

#### Problem :point_down:
The growth of Computer Science has forced the scientific community to award Nobel Prize in CS starting from this year.

Chef knows that the Nobel community is going to award the prize to that person whose research is different from others (i.e. no other researcher should work on the same topic). If there are multiple such people, who work on unique topics, then they will all share the prize. It might also happen that no one wins this time.

Chef also knows the `n` researchers which the community who will be considered for the prize, and the topics in which each of them work.
In total the CS field can be divided into `m` broad topics. Given the topics in which each of the `n` researchers are working on, in the form of an array `a`, and given that Chef can master any topic instantly, find whether he can win the prize. That is, can the Chef choose to work on some topic which will guarantee that he will win the prize? Chef doesn't mind sharing the prize with others.
#### Sample Input :point_down:
```
n = 5
m = 4
a = [4, 2, 1, 1, 1]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
Since only `3` distinct topics (i.e. `1`, `2`, `4`) out of the `m = 4` available have been taken up, Chef can choose the remaining one, i.e, topic `3` to win the prize jointly with the first and the second researcher.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, m, a):
    a = set(a)
    if len(a) < m:
        return True
    else:
        return False
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
[codechef.com](https://www.codechef.com/START2C/problems/NOBEL)
