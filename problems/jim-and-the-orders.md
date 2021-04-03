#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
Jim's Burgers has a line of hungry customers. Orders vary in the time it takes to prepare them. Determine the order the customers receive their orders. Start by numbering each of the customers from to `1` to `n`, front of the line to the back. You will then be given an order number and a preparation time for each customer in an array `o` (orders).

The time of delivery is calculated as the sum of the order number and the preparation time. If two orders are delivered at the same time, assume they are delivered in ascending customer number order.
#### Sample Input :point_down:
```
o = [
    [8, 3],
    [5, 6],
    [6, 2],
    [2, 3],
    [4, 3]
]
```
#### Sample Output :point_down:
```
[4, 5, 3, 1, 2]
```
#### Explanation :point_down:
<img src="https://github.com/menobleknight/coding-problems/blob/main/assets/orders.png" width="250">

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(o):
    p = []
    for i, v in enumerate(o):
        p.append([sum(v), i+1])
        
    p.sort()
    
    o = []
    for i in p:
        o.append(i[1])
        
    return o
```  
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(o):
    return [k[1] for k in sorted([[(v[0]+v[1]), i+1] for i, v in enumerate(o)])]
```  
</details>

#### Solve Here :point_down:
[hackerrank.com](https://www.hackerrank.com/challenges/jim-and-the-orders/problem)
