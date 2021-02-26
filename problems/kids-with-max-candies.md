#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-greedy-wheat)

#### Problem :point_down:
Given the array of candies `c` and the integer  `e` denoting extra candies, where `c[i]` represents the number of candies that the `ith` kid has.  
For each kid check if there is a way to distribute extra candies among the kids such that he or she can have the greatest number of candies among them. Notice that multiple kids can have the greatest number of candies.
#### Sample Input :point_down:
```
c = [2, 3, 5, 1, 3] 
e = 3
```
#### Sample Output :point_down:
```
[true, true, true, false, true] 
```
#### Explanation :point_down:
maximum candies = `5`
```
kid 1 has 2 candies, he will have 5 candies if he gets 3 extra candies.
kid 2 has 3 candies, he will have 5 candies if he gets 2 extra candies.
kid 3 has 5 candies, he will have 5 candies if he gets 0 extra candies.
kid 4 has 1 candies, he will have 4 candies if he gets 3 extra candies.
kid 5 has 3 candies, he will have 5 candies if he gets 2 extra candies.
```
kid 4 will not have maximum `5` candies, it's `false`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c, e):
    a = [False for _ in range(len(c))] # answer

    m = max(c)
    for i in range(len(c)):
        if (c[i] + e) >= m:
            a[i] = True

    return a
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(c, e):
    return [True if (i + e) >= max(c) else False for i in c]
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)
