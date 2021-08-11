#### Topics :point_down:
<img src="https://github.com/er-knight/coding-problems/blob/main/problem-tags/greedy-tag.png" height="22"> <img src="https://github.com/er-knight/coding-problems/blob/main/problem-tags/math-tag.png" height="22">

#### Problem :point_down:
One day Kana gets interested in a new adventure game called Dragon Quest. In this game, her quest is to beat a dragon.
The dragon has a hit point of `h` initially. When its hit point becomes `0` or less than `0`, it will be defeated. 
In order to defeat the dragon, Kana can cast the two following types of spells.
- Void Absorption, which changes dragon's hit point point from `h` to `floor(h / 2) + 10`.
- Lightning Strike, which changes dragon's hit point point from `h` to `h - 10`.

Kana can cast at most `n` Void Absorptions and `m` Lightning Strikes in any order. Return true if it's possible to defeat the dragon else false.

#### Sample Input :point_down:
```
h = 100 
n = 3 
m = 4
```
#### Sample Output :point_down:
```
True
```
#### Explanation :point_down:
One possible casting sequence is given below.
```
👉 Void Absorption   h = 100 → h = floor(h / 2) + 10 = 60
👉 Void Absorption   h = 60  → h = floor(h / 2) + 10 = 40
👉 Void Absorption   h = 40  → h = floor(h / 2) + 10 = 30
👉 Lightning Strikes h = 30  → h = h - 10            = 20
👉 Lightning Strikes h = 20  → h = h - 10            = 10
👉 Lightning Strikes h = 10  → h = h - 10            = 0
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(h, n, m):
    while h > 20 and n > 0:
        h = h // 2 + 10
        n -= 1

    return h <= (10 * m)
```  
#### Explanation :point_down:
It isn't optimal to cast Void Absorptions for `h ≤ 20`, because it doesn't decreases the value of `h`.
- `h = 20` becomes `floor(h / 2) + 10 = 20` after Void Absorptions.
- `h = 17` becomes `floor(h / 2) + 10 = 18` after Void Absorptions.

So, cast all available Void Absorptions until `h` becomes less than or equal to `20`. Then cast all available Lightning Strikes.

#### Time Complexity :point_down:
```
o(n + m)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[codeforces.com](https://codeforces.com/problemset/problem/1337/B)
