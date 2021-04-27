#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-binary--search-wheat)

#### Problem :point_down:
Given an array of integers `a`, sorted in ascending order, and a number `k`, return the index where `k` should be inserted to keep `a` sorted. If `k` already exists in `a`, return the largest index where `k` can be inserted.
#### Sample Input :point_down:
```
a = [1, 2, 4, 5]
k = 3
```
#### Sample Output :point_down:
```
2
```
#### Explanation :point_down:
inserting `k = 3` at index `i = 2` keeps `a` sorted.
```
a = [1, 2, 3, 4, 5]
           ↑
```
<details>
<summary><strong>Solution</strong></summary>

#### Python :point_down:
```py
def solve(a, k):
    i, j = 0, len(a)
    while i < j:
        m = (i+j)//2
        if a[m] <= k:
            i = m + 1
        else:
            j = m

    return i
```  
#### Python :point_down:
```py
def solve(a, k):
    return bisect.bisect(a, k)
```  
#### C++ :point_down:
```cpp
int solve(vector<int>& a, int k) {
    return (upper_bound(a.begin(), a.end(), k) - a.begin());
}
```  
#### Time Complexity :point_down:
```
O(log n)
```
#### Space Complexity :point_down:
```
O(1)
```
</details>

#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Insertion-Index-in-Sorted-List)
