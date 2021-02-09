#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat)

#### Problem :point_down:
Given an array of integers `a` and an integer `k`, return `true` if you can remove exactly one element from the list to make the average equal to exactly `k`.
#### Sample Input :point_down:
```
a = [1, 2, 3, 10]
k = 2
```
#### Sample Output :point_down:
```
true
```
#### Explanation :point_down:
We can take `10` out to reach an average of `2` since `(1 + 2 + 3) / 3 = 2`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, k):
    s = sum(a)
    t = k * (len(a)-1)
    for i in a:
        if (s - i) == t:
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

#### Reference :point_down:
[tutorialspoint.com](https://www.tutorialspoint.com/remove-one-to-make-average-k-in-python)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Just-Average)
