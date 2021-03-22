
#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Vlad built up his own playlist. The playlist consists of `n` songs, each has a unique positive integer length. Vlad likes all the songs from his playlist, but there is a song, which he likes more than the others. It's named "Uncle Johny".

After creation of the playlist, Vlad decided to sort the songs in increasing order of their lengths. For example, if the lengths of the songs in playlist was `[1, 3, 5, 2, 4]` after sorting it becomes `[1, 2, 3, 4, 5]`. Before the sorting, "Uncle Johny" was on `k-th` position (`1`-indexing is assumed for the playlist) in the playlist.

Vlad needs your help! He gives you all the information of his playlist. Your task is to find the position of "Uncle Johny" in the sorted playlist.
#### Sample Input :point_down:
```
a = [1, 3, 4, 2]
k = 2
```
#### Sample Output :point_down:
```
3
```
#### Explanation :point_down:
`k` equals to `2`, `a` equals to `[1, 3, 4, 2]`. The answer is `3`, because `[1, 3, 4, 2]` &rarr; `[1, 2, 3, 4]`. `a[2] = 3` now is on the `3-rd` position.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(a, k):
    s = a[k-1] # song
    a.sort()
    for i in range(len(a)):
        if a[i] == s:
            return (i+1)
```  
#### Time Complexity :point_down:
```
O(n log n)
```
#### Space Complexity :point_down:
```
O(1)
```
#### Python :point_down:
```py
def solve(a, k):
    c = 0
    for i in a:
        if i < a[k-1]:
            c += 1 
            
    return (c + 1) 
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
[codechef.com](https://www.codechef.com/problems/JOHNY)
