#### Topics :point_down:
![](https://img.shields.io/badge/-array-wheat) 
![](https://img.shields.io/badge/-stack-wheat)

#### Problem :point_down:
You are given an array of strings `ops` where each element is either:
- A non-negative integer that should be pushed into a stack
- `"POP"` meaning pop the top element in the stack
- `"DUP"` meaning duplicate the top element in the stack
- `"+"` meaning pop the top two and push the sum
- `"-"` meaning pop the top two and push `top - second`

Return the top element in the stack after applying all operations. If there are any invalid operations, return `-1`.
#### Sample Input :point_down:
```
ops = ["1", "5", "DUP", "3", "-"]
```
#### Sample Output :point_down:
```
-2
```
#### Explanation :point_down:
Following the operations:
```
→ push 1 into the stack: [1]
→ push 5 into the stack: [1, 5]
→ duplicate the top element: [1, 5, 5]
→ push 3 into the stack: [1, 5, 5, 3]
→ pop 3 and 5 and push their difference 3 - 5: [1, 5, -2]

→ return the top element which is -2
``` 
<details>
<summary>Expand</summary>

#### Python :point_down:
```py
def solve(ops):
    stack = []
    for i in ops:
        if i == 'POP':
            if stack:
                stack.pop()
            else:
                return -1
        elif i == 'DUP':
            if stack:
                stack.append(stack[-1])
            else:
                return -1
        elif i == '+':
            if len(stack) < 2:
                return -1
            else:
                stack.append(stack.pop() + stack.pop())
        elif i == '-':
            if len(stack) < 2:
                return -1
            else:
                stack.append(stack.pop() - stack.pop())
        else:
            stack.append(int(i))

    if (stack):
        return stack[-1]

    return -1
```  
#### [@manparvesh](https://binarysearch.com/problems/Word-Machine/editorials/2121501)'s Python Solution :point_down:
```py
def solve(ops):
    stack = []
    try:
        for i in ops:
            if i == 'POP':
                stack.pop()
            elif i == 'DUP':
                stack.append(stack[-1])
            elif i == '+':
                stack.append(stack.pop() + stack.pop())
            elif i == '-':
                stack.append(stack.pop() - stack.pop())
            else:
                stack.append(int(i))

        return stack[-1]

    except:
        return -1
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
[binarysearch.com](https://binarysearch.com/problems/Word-Machine)
