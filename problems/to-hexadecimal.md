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

    c = '0123456789abcdef' # hex-code
    h = ''                 # hexa-decimal
    n = n + (2 ** 32) if (n < 0) else n

    while (n):
        h += c[n % 16]
        n //= 16

    return h[::-1]
```
#### C++ :point_down:
```cpp
string solve(int n) {
    if (n == 0) return "0";

    string c = "0123456789abcdef"; // hex-code
    string h = "";                 // hexa-decimal
    unsigned int m = n;

    while (m) {
        h += c[m % 16];
        m /= 16;
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
