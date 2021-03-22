#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 

#### Problem :point_down:
There is a list of `n` jobs to do before the kitchen can be closed for the night. These jobs are indexed from `1` to `n`.

The Chef and his assistant divide up the remaining jobs in the following manner. The Chef takes the unfinished job with least index, the assistant takes the unfinished job with the second least index, the Chef takes the unfinished job with the third least index, etc. That is, if the unfinished jobs were listed in increasing order of their index then the Chef would take every other one starting with the first job in the list and the assistant would take every other one starting with the second job on in the list. 

The cooks logged which jobs they finished before they left. Unfortunately, these jobs were not recorded in any particular order. Given an unsorted array `c` of completed jobs, you are to determine which jobs the Chef must complete and which jobs his assitant must complete before closing the kitchen for the evening. 
#### Sample Input :point_down:
```
n = 6
m = 3
c = [2, 4, 1]
```
#### Sample Output :point_down:
```
3 6
5
```
#### Explanation :point_down:

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(n, c):
    j = [0 for i in range(n)] # total jobs
    for i in c:
        j[i-1] = 1
        
    r = [] # remaining jobs
    for i in range(n):
        if j[i] == 0:
            r.append(i+1)
    
    c = r[0::2] if r[0::2] else ' ' # chef     
    a = r[1::2] if r[1::2] else ' ' # assistant
            
    return (c, a)
```  
#### Time Complexity :point_down:
```
O(n)
```
#### Space Complexity :point_down:
```
O(n)
```
</details>

#### Solve Here :point_down:
[codechef.com](https://www.codechef.com/problems/CLEANUP)
