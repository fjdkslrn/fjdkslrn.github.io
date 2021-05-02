---
categories: 
   - Algorithm
tags:
   - Codility
   - Counting Elements
---
## 생각의 흐름
1. 배열 A 길이 구하기
2. 배열 A 돌면서 check_set에 추가
3. 1-N set 생성해서 비교.

### 있나 없나 비교는 set이 편하군,

## 1차시도 - 100%

```python
def solution(A):
    length = len(A)

    check_set = set()
    correct_set = set(range(1,length+1))

    for i in A:
        check_set.add(i)

    if check_set == correct_set:
        return 1
    else:
        return 0
```
