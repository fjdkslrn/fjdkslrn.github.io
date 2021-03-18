---
categories: 
   - Algorithm
tags:
   - Codility
   - Time Complexity
---

## 1차 시도 - 30%
정렬은 복잡도가 n^2라고 해서 remove 함수 사용해봄. 

```python
def solution(A):
    aa = [1,2,3,4,5]

    for i in A:
        aa.remove(i)

    return aa[0]
```

---
## 2차 시도 - 100%
그냥 계산
```python
def solution(A):
    num = len(A)

    result = int((num + 2) * (num + 1) / 2)

    for i in A:
        result -= i

    return result
```