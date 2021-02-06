#### Source Code :point_down:

```cpp
vector<string> split(const string& s, const char& delim) {
    vector<string> list;
    stringstream ss(s);
    string word;
    while (getline(ss, word, delim)) {
        if (word.empty())
            continue;
        list.emplace_back(word);
    }
    return list;
}
```

#### Explanation :point_down:

According to [cplusplus.com](http://www.cplusplus.com/reference/string/string/getline/), `getline()` extracts characters from `ss` and stores them into `word` until the delimitation character `delim` is found.  
Let `s = "abc--def-ghi"`. So, `getline()` will extract `a`, `b` and `c` from `ss` and store them into `word` until the delimitation character `-` is found. `"abc"` is added to `list`.  
For next iteration of while loop `word` becomes empty and `getline()` again starts extracting characters from `ss`. We get the delimitation character `-` again.  But now `word` is empty. So, to avoid adding an empty string `word` into `list`, `if (word.empty())` condition is used.  

#### Uses :point_down:

```cpp
#include <iostream>
#include <sstream>
#include <vector>
using namespace std;

vector<string> split(const string& s, const char& delim) {
    vector<string> list;
    stringstream ss(s);
    string word;
    while (getline(ss, word, delim)) {
        if (word.empty())
            continue;
        list.emplace_back(word);
    }
    return list;
}

int main() {
    string s = "abc--def-ghi";
    char delim = '-';
    vector<string> list = split(s, delim);
    for (string i: list) 
        cout << i << " ";
    return 0;
}
```

#### Use Here :point_down:
[leetcode.com](https://leetcode.com/problems/reverse-words-in-a-string/)
