---
categories: 
   - Algorithm
tags:
   - Codility
   - Counting Elements
---
이건 문제가 뭘 의미하는지 몰라서 이해하는데 오래걸렸으므로 문제에 대한 설명도 첨부.

<img src="/assets/images/algorithms/FrogRiverOne.png" width="" height="" title="FrogRiverOne" alt="FrogRiverOne"/> 


## 1차시도 - 36%
못 건너는 경우를 배제 등

```python
def solution(X, A):
    road = list(range(1, X+1))

    if len(road) == 0:
        return 0

    for sec, location in enumerate(A):
        if location in road:
            road.remove(location)
        else:
            pass

        if len(road) == 0:
            return sec
```

---
## 2차시도 - 63%
못건넌 경우 코드 한줄 추가.

```python
def solution(X, A):
    road = list(range(1, X+1))

    if len(road) == 0:
        return 0

    for sec, location in enumerate(A):
        if location in road:
            road.remove(location)
        else:
            pass

        if len(road) == 0:
            return sec

    return -1
```

---
## 3차 시도 - 100%
처음에는 road 집합변수에서 하나씩 빼주는 방법으로 했으나, 없는 값을 제거할때 오류를 또 처리해주어야 해서 input_set에 추가하는 방법으로 하였음.

```python
def solution(X, A):
    road = set(range(1, X+1))
    input_set = set([])

    for index, value in enumerate(A):
        input_set.add(value)

        if road == input_set:
            return index

    return -1
```