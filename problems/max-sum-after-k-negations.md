#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)
![](https://img.shields.io/badge/-sorting-wheat)

#### Problem :point_down:
You are given an array of integers `a` and an integer `k`. Consider an operation where you pick an element in `a` and negate it. Given that you must make exactly `k` operations, return the maximum resulting sum that can be obtained.
#### Sample Input :point_down:
```
a = [1, 0, -5, -3]
k = 4
```
#### Sample Output :point_down:
```
9
```
#### Explanation :point_down:
We can negate `-5` three times and `-3` once to get `[1, 0, 5, 3]` and its sum is `9`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, a, k):
        a.sort()
        for i in range(len(a)):
            if a[i] < 0 and k > 0:
                a[i] = -a[i]
                k -= 1

        if k % 2 == 0:
            return sum(a)
        
        return sum(a) - 2 * min(a)
```
#### Hint :point_down:
- We will get maximum sum by negating minimum number
- If we negate a number odd times, we get same number at the end.
- If we negate a number even times, we get negative of that number.
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Largest-Sum-After-K-Negations)
