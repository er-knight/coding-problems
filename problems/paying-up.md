#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-bit--manipulation-wheat)
![](https://img.shields.io/badge/-dynamic--programming-wheat) 

#### Problem :point_down:
When a mobster approaches you in a dark alley, he asks you for a specific amount of money `m`. You have a wallet `w` in which there are `n` banknotes. You are obliged to show him all the money that you have, but you only need to pay up if he can find a subset of your banknotes whose total value matches his demand i.e, `m`. Since banknotes in Byteland can have any positive integer value smaller than one thousand you are quite likely to get off without paying.

Both the citizens and the gangsters of Byteland have very positive feelings about the system. No one ever gets hurt, the gangsters don't lose their jobs, and there are quite a few rules that minimize that probability of getting mugged (the first one is: don't go into dark alleys - and this one is said to work in other places also). 

Return `true` if there is a subset of `w` that sums to `m`, else `false`.
#### Sample Input :point_down:
```
n = 5
m = 11
w = [1, 2, 4, 8, 16]
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can make total of `11` by taking notes of `1`, `2` and `8`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, m, w):
    d = [[0 for j in range(m+1)] for i in range(n+1)] # dp
    
    for i in range(n+1):
        d[i][0] = 1 
    for i in range(1, m+1):
        d[0][i] = 0
        
    for i in range(1, n+1):
        for j in range(1, m+1):
            if j < w[i-1]:
                d[i][j] = d[i-1][j]
            else:
                d[i][j] = d[i-1][j] or d[i-1][j - w[i-1]]
                
    return d[n][m]
```
#### Time Complexity :point_down:
```
O(n * m)
```
#### Space Complexity :point_down:
```
o(n * m)
```
#### Python :point_down:
```py
def solve(n, m, w):
    for i in range(1<<n): # 1 << n = pow(2, n)
        s = 0 # sum
        for j in range(n):
            if (i & (1<<j)) != 0:
                s += w[j]
            if s == m:
                return True 
                
    return False
```
#### Time Complexity :point_down:
```
O((2 ^ n) * n)
```
#### Space Complexity :point_down:
```
o(1)
```
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/subset-sum-problem-dp-25/)  
[geeksforgeeks.org](https://www.geeksforgeeks.org/find-distinct-subsets-given-set/)
#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/MARCHA1)
