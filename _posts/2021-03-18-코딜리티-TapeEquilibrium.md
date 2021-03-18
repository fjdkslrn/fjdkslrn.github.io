---
categories: 
   - Algorithm
tags:
   - Codility
   - Time Complexity
---

## 1차 시도 - 23% 망
흠..

```python
def solution(A):
    total = 0

    for tape in A:
        total += tape

    average = total / 2

    result = 0
    short_idx = 0

    for idx, tape in enumerate(A):
        result += tape

        if average == result:
            short_idx = idx
            break
        elif average < result:
            short_idx = idx-1
            result -= tape
            break
        else:
            pass

    return abs(result - (total - result))
```

---
## 2차 시도 - 84% 낫베드

```python
def solution(A):
    left_length = 0
    right_length = 0
    total_length = sum(A)
    min_length = 1000000

    for i in A:
        left_length += i
        right_length = total_length - left_length
        min_length = min(min_length, abs(left_length - right_length))

    return min_length
```

---
## 3차 시도 - 100%
고수 친구에게 첨삭. 깔끔

```python
def solution(A):
    result = 0

    left_sum = 0
    right_sum = sum(A)
    
    for index, value in enumerate(A):
        # 마지막 탈출 조건
        if index == (len(A)-1):
            break

        # 레프트 추가
        left_sum += value
        # 라이트 맨 앞 삭제
        right_sum -= value

        # 초기 result
        if index == 0:
            result = abs(left_sum - right_sum)
        else:
            result = min(result, abs(left_sum - right_sum))

    return result
```