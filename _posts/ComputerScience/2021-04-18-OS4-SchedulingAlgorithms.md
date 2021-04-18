---
categories: 
   - ComputerScience
tags:
   - Fastcampus
   - OS
---

# 스케쥴링 알고리즘
---
### 한눈에 보는 흐름
<img src="/assets/images/computerscience/os4.png" width="" height="" title="os4" alt="os4"/>

<br>

### 프로세스란?
- 컴퓨터에서 연속적으로 실행되고 있는 프로그램.
- 프로세스라는 용어는 작업, task, job 이라는 용어와 혼용.
- 응용프로그램 != 프로세스
   - 응용프로그램은 여러개의 프로세스로 이루어질 수 있음.
   - 하나의 응용 프로그램은 여러 개의 프로세스(프로그램)가 상호작용을 하면서 실행될 수도 있음.(?)

<br>

### 스케쥴러란?
- 프로세스의 실행을 관리하는 프로그램(?).

<br>

### 스케쥴링 알고리즘
> 어느 순서대로 프로세스를 실행시킬까

- **FIFO(First in First out)/FCFS(First-Come-First-Served) 스케쥴러**
   + CPU 스케줄링 알고리즘 중에 제일 간단한 알고리즘으로 CPU를 요구하는 순으로 할당하는 방법. FIFO방식인 큐(Queue)로써 구현된다.
<img src="/assets/images/computerscience/fifo.png" width="70%" height="" title="fifo" alt="fifo"/>

- **SJF 스케쥴러**
   + 가장 프로세스 실행시간이 짧은 프로세스부터 먼저 실행을 시키는 방법.
- **우선순위 기반 스케쥴러**
   + 각 프로세스에게 우선 순위를 부여하여 순위가 높은 순서대로 처리하는 방법.
   + 정적/동적 우선순위 가 있음.    
   정적: 우선순위를 미리 지정. / 동적: 스케줄러가 상황에 따라 우선순위를 동적으로 변경.
- **RoundRobin 스케쥴러**
   + 프로세스들 사이에 우선순위를 두지 않고, 순서대로 시간단위(ex. 100ms)로 CPU를 할당하는 방법. 수행시간동안 완료하지 못한 프로세스는 준비큐의 끝으로 밀려남.
<img src="/assets/images/computerscience/rr.png" width="70%" height="" title="rr" alt="rr"/>

<br>

<img src="/assets/images/computerscience/schedulingAlgol.png" width="" height="" title="schedulingAlgol" alt="schedulingAlgol"/>

<br>
<br>

### 📌정리  
- FIFO (FCFS) 스케쥴링 알고리즘 (배치 처리 시스템)
- 최단 작업 우선(SJF) 스케쥴링 알고리즘
- 우선순위 기반 스케쥴링 알고리즘
   + 정적 우선순위, 동적 우선순위
- Round Robin 스케쥴링 알고리즘
   + 시분할 시스템 기반

<br>

>참고/출처:<br>- 패스트캠퍼스 운영체제 강의(Dave Lee 강사님)