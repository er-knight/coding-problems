#### Topics :point_down:
![](https://img.shields.io/badge/-hash--map-wheat)
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given a string `text`, you want to use the characters of `text` to form as many instances of the word `"balloon"` as possible.
You can use each character in `text` at most once. Return the maximum number of instances that can be formed.
#### Sample Input :point_down:
```
text = "loonbalxballpoon"
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
```
l o o n b a l x b a l l p o o n
↑ ↑ ↑ ↑ ↑ ↑ ↑   ↑ ↑ ↑ ↑   ↑ ↑ ↑
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(text):
    d = {'b': 0, 'a': 0, 'l': 0, 'o': 0, 'n': 0}

    for i in text:
        if i in 'balon':
            d[i] += 1

    d['l'] //= 2
    d['o'] //= 2

    return min(d.values())
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
[leetcode.com](https://leetcode.com/problems/maximum-number-of-balloons/)
