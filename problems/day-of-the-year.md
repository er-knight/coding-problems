#### Topics :point_down:
![](https://img.shields.io/badge/-math-wheat)

#### Problem :point_down:
Given a string `date` representing a [`Gregorian calendar`](https://en.wikipedia.org/wiki/Gregorian_calendar) date formatted as `YYYY-MM-DD`, return the day number of the year.
#### Sample Input :point_down:
```
date = "2019-02-10"
```
#### Sample Output :point_down:
```
41
```
#### Explanation :point_down:
```
31 (January) + 10 (February) = 41
```
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(date):
    year, month, day = int(date[:4]), int(date[5:7]), int(date[8:])

    is_leap = True if ((year % 4 == 0) and (year % 100 != 0)) or (year % 400 == 0) else False

    days = [31, (29 if is_leap else 28), 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
    
    day_of_year = sum(days[:month-1]) + day

    return day_of_year
```
</details>

#### Solve Here :point_down:
[leetcode.com](https://leetcode.com/problems/day-of-the-year/)
