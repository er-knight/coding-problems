#### Topics :point_down:
<img src="https://github.com/er-knight/coding-problems/blob/main/problem-tags/math-tag.png" height="22">

#### Problem :point_down:
Given a binary number `x` of `n` bits, find the highest power of 2 that divides `x`.

#### Sample Input :point_down:
```
n = 5
x = 10100
```

#### Sample Output :point_down:
```
2
```

#### Explanation :point_down:
```
👉 2⁰ (= 1)         divides 20 (10100 in binary)
👉 2¹ (= 2)         divides 20 (10100 in binary)
👉 2² (= 4)         divides 20 (10100 in binary)
👉 2³ (= 8) doesn't divides 20 (10100 in binary)

∴ 2 is the highest power of 2, which divides 20. 
```

<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(n, x):
    p = 0
    for i in range(n):
        if x[i] == "1":
            p = i

    return n - p - 1
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
[codechef.com](https://www.codechef.com/problems/MAX2)
