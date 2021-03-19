---
categories: 
   - Algorithm
tags:
   - Codility
   - Time Complexity
---

## 1차 시도 - 44%
그냥 단순하게, 엄청난 타임아웃 에러

Runtime Error
```python
def solution(X, Y, D):
    count = 0
    while X < Y:
        count += 1
        X = X + D

    return count
```

---
## 2차 시도 - 100%
그냥 계산
```python
import math

def solution(X, Y, D):
    count = (Y - X) / D

    return math.ceil(count)
```