---
categories: 
   - Algorithm
tags:
   - Arrays
   - OddOccurrencesInArray
---

## 1차 시도 - 66%
딕셔너리에 key:값, value:카운트 로 해서 리스트 한바퀴 돌고 마지막에 딕셔너리에서 value값이 1인 요소의 key값 리턴

Runtime Error
```python
def solution(A):
    count_dict = {}

    for ele in A:
        if ele in count_dict:
            count_dict[ele] += 1
        else:
            count_dict[ele] = 1

    index = 0
    key_list = list(count_dict.keys())
    for count in count_dict.values():
        if count == 1:
            return key_list[index]
        index += 1
```
인터넷 검색을 통해 key값과 value값을 바꾸는걸 찾아냄. 그걸 적용시켜봄. 그래도 66%;; 
맨 아래 if 부분 가지고도 점수를 까더라.. if i == 1 : 로 했는데 계속 100%가 안뜸.  비교연산보다 나누기가 빠른건가 뭐지..

```python
def solution(A):
    count_dict = {}

    for ele in A:
        if ele in count_dict:
            count_dict[ele] += 1
        else:
            count_dict[ele] = 1

    change_dic = {v: k for k, v in count_dict.items()}
    
    tmp_index = change_dic.keys()

    for i in tmp_index:
        if (i % 2) != 0 :
            return change_dic[i]
```
---
## 2차 시도 - 66%
왜지;;  시간 복잡도가 O(N**2) 라네
```python
def solution(A):
    empty_list = []

    for ele in A:
        if ele in empty_list:
            empty_list.remove(ele)
        else:
            empty_list.append(ele)

    return empty_list[0]
```
---
## 그 외 풀이들
XOR 로 푸는 방법도 있다고함
```python
def solution(A):
    N = len(A)
    if N<2:
        return A[0]

    A_sort = sorted(A)
    count = 1
    a = A_sort[0]

    for i in range(1, N):
        if A_sort[i] == a:
            count += 1
        else: #A_sort[i] != a
            if count%2 == 0:
                count = 1
                a = A_sort[i]
            else:
                return a

    return a
```