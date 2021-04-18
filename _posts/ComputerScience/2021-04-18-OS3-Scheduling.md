---
categories: 
   - ComputerScience
tags:
   - Fastcampus
   - OS
---

# 스케쥴링
---

### 배치 처리 시스템
컴퓨터 프로그램 실행 요청 순서에 따라 순차적으로 프로그램을 실행하는 방식.  
한번에 등록된 여러 프로그램을 순차적으로 실행 가능.  
  
**문제점)**  
💣 어떤 프로그램의 실행시간이 오래 걸려서, 다른 프로그램 실행까지 오래 기다려야 한다.  
ex) App1(12시간), App2(30분)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**-> App2 실행완료까지 12시간 30분 ;;**  
💣 동시에 여러 응용프로그램 실행.  
ex) 음악을 들으며, 문서작업을 하고 싶다.  
💣 다중 사용자 지원은??..
> 그래서 **멀티프로그래밍/시분할시스템**이 나왔다.

<br>

### 시분할 시스템
다중 사용자 지원을 위해 컴퓨터 응답 시간을 최소화하는 시스템.  
<img src="/assets/images/computerscience/timesharing.png" width="" height="" title="timesharing" alt="timesharing"/> 

<br>

### 멀티 태스킹
단일 CPU에서, 여러 응용 프로그램이 동시에 실행되는 것 처럼 보이도록 하는 시스템.
<img src="/assets/images/computerscience/multitasking.png" width="" height="" title="multitasking" alt="multitasking"/> 

<br>

### 멀티 태스킹과 멀티 프로세싱
**멀티태스킹** -> 단일 CPU  
**멀티프로세싱** -> 여러 CPU에 하나의 프로그램을 병렬로 실행해서 실행속도를 빠르게
<img src="/assets/images/computerscience/multiprocessing.png" width="" height="" title="multiprocessing" alt="multiprocessing"/> 

<br>

### 멀티 프로그래밍
- 최대한 CPU를 많이 활용하도록 하는 시스템
&nbsp;-> 시간 대비 CPU 활용도 UP.
-  응용프로그램은 온전히 CPU를 쓰기 보다, 중간에 다른 작업을 필요로 하는 경우가 많다.
&nbsp;-> 응용프로그램이 실행되다가 파일을 읽거나, 프린팅을 한다.  
&nbsp;**=>다른 자원을 사용하는 작업을 하는동안 다른 응용프로그램을 실행하도록 한다**
<img src="/assets/images/computerscience/multiprogramming.png" width="" height="" title="multiprogramming" alt="multiprogramming"/> 

<br>

### 📌정리
> 시분할시스템, 멀티프로그래밍, 멀티태스킹이 유사한 의미로 통용.

**핵심**  
1️⃣ 여러 응용프로그램 실행을 가능토록 함.  
2️⃣ 응용프로그램이 동시에 실행되는 걱처럼 보이도록 함.  
3️⃣ CPU를 쉬지 않고 응용프로그램을 실행토록 해서, 짧은 시간 안에 응용프로그램이 실행완료될 수 있도록 함.  
4️⃣ 컴퓨터 응답시간도 짧게해서, 다중 사용자도 지원.  

- 배치 처리 시스템: 여러 응용프로그램을 순차적으로 처리하는 시스템.
- 시분할 시스템: 다중 사용자 지원, 컴퓨터 응답시간을 최소화하는 시스템
- 멀티 태스킹: 단일 CPU에서 여러 응용 프로그램을 동시에 실행하는 것처럼 보이게 하는 시스템
- 멀티 프로세싱: 여러 CPU에서 하나의 응용 프로그램을 병렬로 실행하게 해서, 실행속도를 높이는 기법
- 멀티 프로그래밍: 최대한 CPU를 일정 시간당 많이 활용하는 시스템

<br>

>참고/출처:<br>- 패스트캠퍼스 운영체제 강의(Dave Lee 강사님)<br>- 멀티프로세싱이미지(http://donghoson.tistory.com/15)