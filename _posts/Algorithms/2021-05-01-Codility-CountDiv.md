---
categories: 
   - Algorithm
tags:
   - Codility
   - Prefix Sums
---
## 생각의 흐름
1. A, B를 K로 나눈 후
2. A 나머지 OX, B 나머지 OX 4가지 케이스 생각
3. 올림해서 뒤에서 앞에 뺌.

## 1차시도 - 37%

```python
import math

def solution(A, B, K):
    div_a = math.ceil(A / K)
    div_b = math.ceil(B / K)

    if (A%K == 0) and (B%K != 0):
        return (div_b - div_a)
    else:
        return (div_b - div_a + 1)
```

##그냥 나눠서 나머지 0일때도 해봤는데 숫자가 커졌을때 타임아웃에러 발생함..!

## 2차시도 - 50%
;;;
```python
def solution(A, B, K):
    div_a = A // K
    div_b = B // K

    if B < K:
        return 0
    elif B == K:
        return 1
    else:
        if A >= K:
            if (A % K) != 0 and (B % K == 0):
                return div_b - div_a
            else:
                return div_b - div_a +1
        else:
            return div_b - div_a
```

