#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-hash--map-wheat) 
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
A newly designed keypad was tested, where a tester pressed a sequence of `n` keys, one at a time.  
You are given a string `k` of length `n`, where `k[i]` was the `ith` key pressed in the testing sequence, and a sorted list `r`, where `r[i]` was the time the `ith` key was released. Both arrays are `0-indexed`. The `0th` key was pressed at the time `0`, and every subsequent key was pressed at the exact time the previous key was released.  
The tester wants to know the key of the keypress that had the longest duration. The `ith` keypress had a duration of `r[i] - r[i-1]`, and the `0th` keypress had a duration of `r[0]`.  
Note that the same key could have been pressed multiple times during the test, and these multiple presses of the same key may not have had the same duration.  
Return the key of the keypress that had the longest duration. If there are multiple such keypresses, return the lexicographically largest key of the keypresses.
#### Sample Input :point_down:
```
r = [9, 29, 49, 50]
k = "cbcd"
```
#### Sample Output :point_down:
```
"c"
```
#### Explanation :point_down:
The keypresses were as follows:
```
Keypress for 'c' had a duration of 12 -  0 = 12
Keypress for 'b' had a duration of 29 -  9 = 20
Keypress for 'c' had a duration of 49 - 29 = 20
Keypress for 'd' had a duration of 50 - 49 =  1
```
The longest of these was the keypress for `'c'` and `'b'` with duration `20`.  
`'c'` is lexicographically larger than `'b'`, so the answer is `'c'`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(r, k):
    d = {k[0]: r[0]} 
    for i in range(1, len(r)):
        d[k[i]] = max(d.get(k[i], 0), r[i]-r[i-1])

    print(d)
    m = max(d.values())
    return max([i for i in d if d[i] == m])
```
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
#### Python :point_down:
```py
def solve(r, k):
    c = k[0] # key
    t = r[0] # time

    for i in range(1, len(r)):
        if (r[i] - r[i-1]) > t:
            t = r[i] - r[i-1]
            c = k[i]
        elif (r[i] - r[i-1]) == t and k[i] > c:
            c = k[i]

    return c
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
[leetcode.com](https://leetcode.com/problems/slowest-key/)
