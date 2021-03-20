#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Today is Chef's birthday. His mom has surprised him with truly fruity gifts: 2 fruit baskets. The first basket contains `n` apples, and the second one contains `m` oranges. Chef likes apples and oranges very much but he likes them equally, and therefore, wants to have the minimum possible difference between the number of apples and oranges he has. To do so, he can purchase `1` apple or `1` orange by paying exactly `1` gold coin (that's some expensive fruit, eh?). Chef can purchase fruits at most `k` times (as he has only `k` gold coins in his pocket) to make the difference the minimum possible.

Our little Chef is busy in celebrating his birthday to the fullest, and therefore, he has handed this job to his best friend — you. Can you help him by finding the minimum possible difference he can achieve between the number of apples and orange he owns? 
#### Sample Input :point_down:
```
n = 5 
m = 2 
k = 1
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
Chef will buy `1` orange by paying `1` gold coin and will have `5` apples and `3` oranges.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, m, k):
    d = abs(n - m) # difference
    if k >= d:
        return 0

    return (d - k) 
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

#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/FRUITS)