# Code
## Data Structure
### Stack in Python
``` 
# Using deque
from collections import deque
myStack = deque()
myStack.append('a')
myStack.pop()

# Using list
myStack = []
myStack.append('a')
myStack.pop()
```
Deque is built upon a <u>**double linked list**</u>. In a linked list structure, each entry is stored in its own memory block and has a reference to the next entry in the list. The <u>**constant time**</u> .append() and .pop() operations make deque an excellent choice for implementing a Python stack if code doesn’t use threading.

However, <u>**list**</u> is built upon <u>**blocks of contiguous memory**</u>. If the block of contiguous memory is full, then it will need to get another block, which can take much longer than a normal .append().

### Deque(双端队列) in Python

双端队列适用于滑窗问题，同样使用 collections 的 deque
>**Leetcode 239. Sliding Window Maximum**
>Given an array nums, there is a sliding window of size k which is moving from the very left of the array to the very right. You can only see the k numbers in the window. Each time the sliding window moves right by one position. Return the max sliding window.
>Input: nums = [1,3,-1,-3,5,3,6,7], and k = 3
Output: [3,3,5,5,6,7] 
