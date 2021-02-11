#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
There is a sequence of words in camelCase as a string of letters, having the following properties:
- It is a concatenation of one or more words consisting of English letters.
- All letters in the first word are lowercase.
- For each of the subsequent words, the first letter is uppercase and rest of the letters are lowercase.

Given `s`, determine the number of words in `s`.
#### Sample Input :point_down:
```
s = "saveChangesInTheEditor"
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
`s` contains `5` words: `save`, `Changes`, `In`, `The` and `Editor`.

<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(s):
    words = 1
    for i in s:
        if (i.isupper()):
            words += 1
            
    return words
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
[hackerrank.com](https://www.hackerrank.com/challenges/camelcase/problem)
#### Similar Problems :point_down:
[binarysearch.com](https://binarysearch.com/problems/camelCase)
