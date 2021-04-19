---
categories: 
   - ComputerScience
tags:
   - Fastcampus
   - OS
---

# 프로세스 상태와 스케쥴링
---

### 멀티프로그래밍과 Wait
- 멀티프로그래밍: CPU 활용도를 극대화 하는 스케쥴링 기술
- Wait: 간단한 예로 저장매체로부터 파일 읽기를 기다리는 시간으로 가정.  
**프로세스 A/B/C가 실행/대기 등으로 상태가 바뀜.**

<img src="/assets/images/computerscience/multiWait.png" width="70%" height="" title="multiWait" alt="multiWait"/>

<br>

### 프로세스 상태
<img src="/assets/images/computerscience/processStatus.png" width="70%" height="" title="processStatus" alt="processStatus"/>

- ready: CPU에서 실행 가능 상태(실행 대기 상태)
- running: CPU에서 실행중 상태.
- block: 특정 이벤트 발생 대기 상태. ex) 저장매체 파일읽기 완료.

<br>

### 프로세스 상태 간 관계
CPU 처리 순서 연습해보기!! 가장 기본적인 Queue + 시분할

<img src="/assets/images/computerscience/processExercise.png" width="70%" height="" title="processExercise" alt="processExercise"/>

<br>

>참고/출처:<br>- 패스트캠퍼스 운영체제 강의(Dave Lee 강사님)