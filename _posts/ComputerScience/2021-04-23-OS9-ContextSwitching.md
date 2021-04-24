---
categories: 
   - ComputerScience
tags:
   - Fastcampus
   - OS
---

# 컨텍스트 스위칭
---

### 컨텍스트 스위칭
> 하나의 프로세스가 CPU를 사용 중인 상태에서 다른 프로세스가 CPU를 사용하도록 하기 위해, 이전의 프로세스의 상태(문맥)를 보관하고 새로운 프로세스의 상태를 적재하는 작업. <br><br>한 프로세스의 문맥은 그 프로세스의 **프로세스 제어블록(PCB)**에 기록되어 있음.

<br>

### 프로세스 제어블록(PCB)
> 특정한 프로세스에 대한 정보를 포함하는 운영 체제 커널의 자료 구조이다. 프로세스가 실행중인 상태를 캡쳐/구조화해서 저장.<br>Ex) Process ID, Register값(SP/PC), Process State, 등등.

<br>

### 컨텍스트 스위칭의 예
<img src="/assets/images/computerscience/contextSwitching.png" width="70%" height="" title="contextSwitching" alt="contextSwitching"/>

- Running 상태의 프로세스 A를 Ready/Block 상태로 변경하고, Ready 상태의 다른 프로세스 B를 Running 상태로 바꿈.
- 바꿀때의 상태.
   + 현재 CPU의 PCB에는 A의 PCB 정보가 들어가있음.
   + B를 실행시키기 위해서, CPU의 PCB에 B의 PCB 정보를 업데이트 침.
- 수정 해야 할 수도... 질문 남겨둔 상태.

<br>

### 용어) 디스패치
> Ready 상태의 프로세스를 Running 상태로 바꾸는것.

<br>


>참고/출처:<br>- 패스트캠퍼스 운영체제 강의(Dave Lee 강사님)