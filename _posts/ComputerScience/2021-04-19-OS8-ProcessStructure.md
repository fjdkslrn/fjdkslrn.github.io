---
categories: 
   - ComputerScience
tags:
   - Fastcampus
   - OS
---

# 프로세스 구조
---

### 프로세스의 구조
- TEXT(CODE) : 코드가 컴파일 되어 저장.
- DATA : 변수 / 초기화된 데이터가 저장.
- STACK : 임시 데이터가 저장. (함수 호출, 로컹 변수 등)
- HEAP : 코드에서 동적으로 만들어지는 데이터가 저장.

<img src="/assets/images/computerscience/processStructure.png" width="20%" height="" title="processStructure" alt="processStructure"/>


### 프로세스에 데이터들이 어떻게 저장되고 실행되는지 연습 문제들

<br>

#### 💡중요 레지스터들
- PC(Program Counter): 실행 할(하는?) CODE영역의 주소를 가리킴. 기본적으로는 주소가 1씩 늘어남.
- SP(Stack Pointer): STACK영역의 마지막(입력될) 부분의 주소를 가리킴.
- EBP: 호출된 함수의 값들 중 최상단 스택포인터의 값을 입력. (돌아갈 주소를 기억해두기 위해)
- EAX: 함수실행 후 반환값을 저장.

- **컴퓨터 구조와 함께 보는 프로세스 구조.**
   <img src="/assets/images/computerscience/processStructureExer.png" width="70%" height="" title="processStructureExer" alt="processStructureExer"/>

<br>

- **Heap 영역을 활용하는 프로세스 구조.**
   <img src="/assets/images/computerscience/processStructureExer2.png" width="70%" height="" title="processStructureExer2" alt="processStructureExer2"/>

<br>

- **Data 영역은 두가지로 나눠짐. BSS / Data**
   - BSS: 초기화되지 않은 전역변수. / DATA: 초기값이 있는 전역변수.
   <img src="/assets/images/computerscience/processStructureExer4.png" width="70%" height="" title="processStructureExer4" alt="processStructureExer4"/>

<br>


>참고/출처:<br>- 패스트캠퍼스 운영체제 강의(Dave Lee 강사님)