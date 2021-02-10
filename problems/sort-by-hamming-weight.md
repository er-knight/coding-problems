#### Topics :point_down:
![](https://img.shields.io/badge/-sorting-wheat) ![](https://img.shields.io/badge/-bit--manipulation-wheat)

#### Problem :point_down:
You are given an array of non-negative integers `a`. Sort the array in ascending order by the number of `1`'s in binary representation for each number. If there are ties in the number of `1`'s, then break ties by their value in ascending order.
#### Sample Input :point_down:
```
a = [3, 1, 4, 7]
```
#### Sample Output :point_down:
```
[1, 4, 3, 7]
```
#### Explanation :point_down:
```
1 (0001) and 4 (0100) both have one 1's but 1 comes earlier since it has lower value.  
3 (0011) has two 1's and 7 (0111) has three 1's.
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a):
    b = []
    for i in a:
        c = 0
        n = i
        while (n):
            n &= (n-1)
            c += 1
        b.append((c, i))

    b.sort()
    a = [i[1] for i in b]
    return a
```
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
o(n)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Sort-List-by-Hamming-Weight)  
[leetcode.com](https://leetcode.com/problems/sort-integers-by-the-number-of-1-bits/)
