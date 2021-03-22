#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given a string `s` of `"a"` and `"b"`s. `"a"`s can stay `"a"` or turn into `"b"`, but `"b"`s can't change.
Return the number of unique strings that can be made.
#### Sample Input :point_down:
```
s = "abba"
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
We can make these strings:
- `"abba"`
- `"abbb"`
- `"bbba"`
- `"bbbb"`

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s):
    return 2 ** s.count('a')
```
#### Hint :point_down:
- Consider only `'a'`s while making subsets.
- An array with `n` elements has `2 ^ n` subsets.
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
[binarysearch.com](https://binarysearch.com/problems/Unique-Ab-Strings)
