---
categories: 
   - Algorithm
tags:
   - Inflearn
   - Tips
---
## 알고리즘 팁들

- 숫자 여러개 입력
    ```python
    a, b = map(int, input("입력: ").split())
    ```
- 숫자 크기 비교할 때 팁
    ```python
    if n>3 and n<9:
    # 위 비교를 아래처럼 써도 됨.
    if 3<n<9:
    ```
- range로 리스트 만들 때
    ```python
    # 1부터 n까지 리스트
    # n+1 까지로 해줘야한다
    range(1, n+1)  # [1, 2, 3, 4, ..., n]

    # 역순으로 리스트 만들고 싶을때
    range(10, 0, -1)  # [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
    ```
- for else 구문
    ```python
    # for 문을 돌다 다 돌고 종료하면 else를 실행하고,
    # 중간에 break로 중단되면 else 실행하지 않음.
    for i in range(1, 11):
        print(i)
        if i>15:
            break
    else:
        print(11)
    ```
- 문자열 관련 함수
    ```python
    msg="test message"

    msg.upper()  # 대문자
    msg.lower()  # 소문자
    msg.find('t')  # t의 위치 인덱스 출력
    msg.count('t')  # t 갯수 카운트
    msg[3:5]  # 인덱스 3~5 골라
    len(msg) # 문자열 길이(공백포함)
    isupper() / islower() / isalpha()  # 각각 대문자일때 소문자일때 문자일때 true 리턴
    ord('A')  # 아스키코드 출력 A는 65, Z는 90. a는 97, z는 122
    chr(65)  # 아스키코드를 문자로
    ```
- 리스트 관련 함수
    ```python
    # 리스트 값 추가
    a.append(6)  # 그냥 맨 뒤에 추가
    a.insert(3, 7)  # 인덱스 3에 7 추가

    # 값 제거
    a.pop()  # 맨 뒤에 값 제거
    a.pop(3)  # 인덱스 3의 값 제거
    a.remove(4)  # 값 4를 찾아서 제거   여러개 다 제거하나??
    
    a.index(5) # 값 5의 인덱스를 출력

    sum(a)  # 리스트의 모든 값의 합
    max(a) / min(a)  # 리스트의 max/min

    r.shuffle(a)  #  막 섞어
    a.sort()  # 오름차순 정렬
    a.sort(reverse=True)  # 내림차순 정렬    

    a.clear()  # 리스트 날리기

    # 인덱스와 값을 한번에 사용하기
    for x in enumerate(a):
        print(x)

    # 모든 조건 참일 경우
    if all(50>x for x in a):
        print("true")
    else:
        print("no")

    # 하나라도 참일 경우
    if any(50>x for x in a):
        print("true")
    else:
        print("no")

    # 특정 길이의 0으로 초기화된 리스트
    a = [0]*10
    ```
- 2차원 리스트 관련
    ```python
    # 2차원 리스트 선언
    a = [[0]*3 for _ in range(3)]

    # 2차원 리스트 출력
    for x in a:
        for y in x:
            print(y, end=' ')
        print()

    
    ```
- 순열느낌(?!)
    ```python
    # 이렇게 하면 순열임. 중복없이 하나씩 뽑는것.
    for i in range(n):
        for j in range(i+1, n):
            for m in range(j+1, n):
                print(i, j, m)
    ```
- 최소값 구할때 팁
    ```python
    arr=[1,2,3,4,5]

    # 1. 무한대로 해놓고 처음부터 비교
    arr_min=float('inf')
    for i in range(len(arr)):

    # 2. 배열의 첫번째 값을 넣고 그 다음부터 비교
    arr_min=arr[0]
    for i in range(1, len(arr)):

        # 여기 if에서 같은지(=등호)를 포함하냐 안하냐에 따라서 마지막 최솟값/처음 최솟값 의 인덱스가 달라질 수 있음.
        # 문제에서 요구하는걸 잘 보면 좋을것.
        if arr[i]<arr_min:
            arr_min=arr[i]
    ```