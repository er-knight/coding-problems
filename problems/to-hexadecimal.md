#### Topics :point_down:
![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
Given an integer `n`, write an algorithm to convert it to hexadecimal. For negative integer, two’s complement method is used. 
#### Sample Input :point_down:
```
n = 26
```
#### Sample Output :point_down:
```
"1a"
```

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n):
    if (n == 0):
        return '0'

    k = 4294967295 # 32-bit unsigned int max value
    n = (k + 1 + n) if (n < 0) else n
    h = '' # hexa-decimal
    while (n):
        m = n % 16
        if (m < 10):
            h += chr(48 + m)
        else:
            h += chr(87 + m)

        n //= 16

    h = h[::-1]

    return h
```
#### C++ :point_down:
```cpp
string solve(int n) {
    unsigned int k = n;
    string h = ""; // hexa-decimal
    if (k == 0) return "0";
    while (k) {
        int m = k % 16;
        if (m < 10) {
            h += (48 + m);
        }
        else {
            h += (87 + m);
        }
        k /= 16;
    }
    reverse(h.begin(), h.end());
    return h;
}
```  
</details>

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/program-decimal-hexadecimal-conversion/)
#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/convert-a-number-to-hexadecimal/)
