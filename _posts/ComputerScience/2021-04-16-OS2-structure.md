---
categories: 
   - ComputerScience
tags:
   - Fastcampus
   - OS
---

# 운영체제 구조
---
<img src="/assets/images/computerscience/os.png" width="" height="" title="os" alt="os"/> 

### 1. User가 Application을 통해 어떠한 작업을 요청한다. ex) 파일 읽기
### 2. Application은 API(->System Call)를 통해 OS에 요청.
### 3. OS는 필요한 하드웨어에서 작업 또는 데이터를 가져다가 돌려줌.

> **API**: 각 언어별 운영체제 기능을 호출하는 인터페이스 함수.  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(필요한 운영체제 기능을b 호출하는 System Call을 호출)  
> **System Call**: 운영체제 기능을 호출하는 함수.  
> **Shell**: 사용자가 운영체제 기능과 서비스를 조작할 수 있도록 인터페이스를 제공하는 프로그램. 터미널 환경(CLI)과 GUI환경 두 종류로 분류.

### 📌정리
- 운영체제는 컴퓨터 하드웨어와 응용 프로그램을 관리한다.
- 사용자 인터페이스를 제공하기 위해 쉘 프로그램을 제공한다.
- 응용프로그램이 운영체제 기능을 요청하기 위해서, 운영체제는 시스템 콜을 제공한다.
   - 보통 시스템 콜을 직접 사용하기 보다는, 해당 시스템 콜을 사용해서 만든 각 언어별 라이브러리(API)를 사용한다.

---

### CPU Protection Rings
<img src="/assets/images/computerscience/cpuProtectionRings.png" width="" height="" title="cpuProtectionRings" alt="cpuProtectionRings"/> 

### 커널모드에서만 실행 가능한 기능들이 있음.
### 커널모드로 실행하려면, 반드시 시스템 콜을 사용해야함(거쳐야함)

### 사용자모드와 커널모드 예시
- 주민등록등본은 꼭 동사무소 또는 민원24시(정부 사이트)에서 특별한 신청서를 써야만, 발급
- 동사무소 직원분들은 특별한 권한을 가지고, 주민등록등본 출력 명령을 실행

### 📌정리
- 운영체제는 시스템 콜 제공
- 프로그래밍 언어별로 운영체제 기능을 활용하기 위해, 시스템 콜을 기반으로 API 제공
- 응용프로그램은 운영체제 기능 필요시, 해당 API를 사용해서 프로그램을 작성
- 응용프로그램이 실행되서, 운영체제 기능이 필요한 API를 호출하면, 시스템 콜이 호출되서, **커널모드로 변경되어** OS내부에서 해당 명령이 실행되고, 다시 응용 프로그램으로 돌아간다.

<br>

>참고/출처:<br>- 패스트캠퍼스 운영체제 강의(Dave Lee 강사님)