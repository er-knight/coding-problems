#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
Lisa just got a new math workbook. A workbook contains exercise problems, grouped into chapters. Lisa believes a problem to be special if its index (within a chapter) is the same as the page number where it's located. The format of Lisa's book is as follows:
- There are `n` chapters in Lisa's workbook, numbered from `1` to `n`.
- The `ith` chapter has `a[i]` problems, numbered from `1` to `a[i]`.
- Each page can hold up to `k` problems. Only a chapter's last page of exercises may contain fewer than `k` problems.
- Each new chapter starts on a new page, so a page will never contain problems from more than one chapter.
- The page number indexing starts at `1`.

Given the details for Lisa's workbook, can you count its number of special problems?
#### Sample Input :point_down:
```
n = 5
k = 3
a = = [4, 2, 6, 1, 10]
```
#### Sample Output :point_down:
```
4
```
#### Explanation :point_down:
The diagram below depicts Lisa's workbook with `n = 5` chapters and a maximum of `k = 3` problems per page. Special problems are outlined in red, and page numbers are in yellow squares.  
<img src="https://s3.amazonaws.com/hr-challenge-images/17892/1456473832-d122786d1e-bear_workbook.png" width="500">  
There are `4` special problems and thus we print the number `4` on a new line.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def workbook(n, k, a):
    s = 0 # special problems
    c = 0 # chapter number
    p = 1 # page number
    q = 1 # problem number

    while c < n:
        if q <= p and p <= min(q+k-1, a[c]):
            s += 1
        p += 1
        q += k
        if q > a[c]: # next chapter
            c += 1
            q = 1
    
    return s
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
[hackerrank.com](https://www.hackerrank.com/challenges/lisa-workbook/problem)
