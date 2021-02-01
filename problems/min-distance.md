#### Topics :point_down:
![](https://img.shields.io/badge/-string-wheat)

#### Problem :point_down:
Given the strings `text`, `word0`, and `word1`, return the smallest distance between any two occurrences of `word0` and `word1` in text, measured in number of words. If either `word0` or `word1` doesn't appear in `text`, return `-1`.
#### Sample Input :point_down:
```
text = "dog cat hello cat dog dog hello cat world"
word0 = "hello"
word1 = "world"
```
#### Sample Output :point_down:
```
1
```
#### Explanation :point_down:
There's only one word `"cat"` in between the `"hello"` and `"world"` at the end.
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(text, word0, word1):
    if (word0 == word1):
        return 0

    words = text.split()
    min_dis = len(words) + 1

    word0_flag = False
    word1_flag = False
    for i in words:
        if (i == word0):
            word0_flag = True
        elif (i == word1):
            word1_flag = True

    if not(word0_flag) or not(word1_flag):
        return -1

    i = 0
    while (i < len(words)): 
        if (words[i] == word0 or words[i] == word1): 
            word_index = i 
            break
        i += 1

    while (i < len(words)): 
        if (words[i] == word0 or words[i] == word1): 
            if (words[word_index] != words[i]):
                min_dis = min(min_dis, (i - word_index - 1))
            word_index = i 
        i += 1       

    return min_dis
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

#### Reference :point_down:
[geeksforgeeks.org](https://www.geeksforgeeks.org/minimum-distance-between-words-of-a-string/)
#### Solve Here :point_down:
[binarysearch.com](https://binarysearch.com/problems/Minimum-Distance-of-Two-Words-in-a-Sentence)
