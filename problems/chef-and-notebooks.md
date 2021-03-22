#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Chef likes to write poetry. Today, he has decided to write a `x` pages long poetry, but unfortunately his notebook has only `y` pages left in it. Thus he decided to buy a new notebook and went to the stationary shop. Shopkeeper showed him some `n` notebooks, where the number of pages and price of the `ith` one are `p[i]` pages and `c[i]` rubles respectively. Chef has spent some money preparing for Ksen's birthday, and then he has only `k` rubles left for now.

Chef wants to buy a single notebook such that the price of the notebook should not exceed his budget and he is able to complete his poetry.

Help Chef accomplishing this task. You just need to tell him whether he can buy such a notebook or not. Note that Chef can use all of the `y` pages in the current notebook, and Chef can buy only one notebook because Chef doesn't want to use many notebooks.
#### Sample Input :point_down:
```
x = 3 
y = 1
k = 2
n = 2
p = [3, 4]
c = [2, 2]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
In this case, Chef wants to write `x = 3` pages long poetry, but his notebook has only `y = 1` page. And his budget is `k = 2` rubles, and there are `n = 2` notebooks in the shop. The first notebook has `p[0] = 3` pages, but Chef cannot buy it, because its price is `c[0] = 4` rubles. The second notebook has `p[1] = 2` pages, and its price is `c[1] = 2` rubles. Thus Chef can select the second notebook to accomplish the task. He will write `1` page of poetry in the old notebook, and `2` page of poetry in the new notebook.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(x, y, k, p, c):
    r = x - y # required pages
    for i in range(len(p)):
        if p[i] >= r and c[i] <= k:
            return True 
            
    return False
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
[codechef.com](https://www.codechef.com/problems/CNOTE)
