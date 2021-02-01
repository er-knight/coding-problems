#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
You are given a string `s` containing digits from `"0"` to `"9"` and lowercase alphabet characters. Return the sum of the numbers found in `s`.
#### Sample Input :point_down:
```
s = "11aa32bbb5"
```
#### Sample Output :point_down:
```
48
```
#### Explanation :point_down:
Since `11 + 32 + 5 = 48`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(self, s):
    sum_ = 0
    n = 0
    for i in s:
        if (i.isdigit()):
            n = n * 10 + int(i)
        else:
            sum_ += n
            n = 0

    return sum_ + n
```
#### C++ :point_down:
```cpp
int solve(string s) {
    int sum_ = 0, n = 0;
    for (char i: s) {
        if (isdigit(i)) {
            n = n * 10 + (i - '0');
        }
        else {
            sum_ += n;
            n = 0;
        } 
    }
    return sum_ + n;
}
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
[binarysearch.com](https://binarysearch.com/problems/ASCII-String-to-Integer)
