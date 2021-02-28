#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)
![](https://img.shields.io/badge/-two--pointer-wheat)

#### Problem :point_down:
Given an array of characters `c`, compress it using the following algorithm.  
Begin with an empty string `s`. For each group of consecutive repeating characters in `c`:
- If the group's length is 1, append the character to `s`.
- Otherwise, append the character followed by the group's length.

The compressed string `s` should not be returned separately, but instead be stored in the input character array `c`. Note that group lengths that are `10` or longer will be split into multiple characters in `c`.  

After you are done modifying the input array, return the new length of the array.  

Could you solve it using only `O(1)` extra space?
#### Sample Input :point_down:
```
c = ["a","a","b","b","c","c","c"]
```
#### Sample Output :point_down:
```
6
```
#### Explanation :point_down:
First `6` characters of the input array should be: `["a","2","b","2","c","3"]`.  
The groups are `"aa"`, `"bb"`, and `"ccc"`. This compresses to `"a2b2c3"`.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(c):
    chr_p = 0 # character pointer
    cnt_p = 1 # count pointer 
    count = 1 
    
    for i in range(1, len(c)):
        if c[i] == c[i-1]:
            count += 1
        else:
            c[chr_p] = c[i-1]
            if count > 1:
                for i in str(count):
                    c[cnt_p] = i
                    cnt_p += 1
            chr_p = cnt_p
            cnt_p += 1
            count = 1

    c[chr_p] = c[-1]
    if count > 1:
        for i in str(count):
            c[cnt_p] = i
            cnt_p += 1

    return cnt_p
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
[leetcode.com](https://leetcode.com/problems/string-compression/)
