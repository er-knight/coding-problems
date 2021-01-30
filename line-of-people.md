#### Topics :point_down:
[<img src="https://img.shields.io/badge/-math-wheat">](https://github.com/topics/math)

#### Problem :point_down:
You are given integers `n`, `a` and `b`. You are standing in a line of `n` people. You don't know which position you're in, but you know there are at least `a` people in front of you and at most `b` people behind you.

Return the number of possible positions you could be in.

#### Sample Input :point_down:
```
n = 10
a = 3
b = 4
```
#### Sample Output :point_down:
```
5
```
#### Explanation :point_down:
There's 10 people and at least 3 are in front and at most 4 are behind.  
This means you can be in indexes `[0, 1, 2, 3, 4]`. For example, at index 0, 9 people are in front, 0 are behind.

<details>
<summary>Expand</summary>

#### Python :point_down:

```py
def solve(n, a, b):
      return min((n-a), b+1)
```
#### C++ :point_down:

```cpp
int solve(int n, int a, int b) {
    return min((n-a), b+1);
}
```
#### JavaScript :point_down:
```js
function solve(n, a, b) {
    return Math.min((n-a), (b+1));
}
```
#### TypeScript :point_down:

```ts
function solve(n: number, a: number, b: number): number {
    return Math.min((n-a), (b+1));
}
```
</details>

#### Solve Here
[binarysearch.com](https://binarysearch.com/problems/Line-of-People)
