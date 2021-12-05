# NagiosMonitoring Project
![nagios 이미지](https://user-images.githubusercontent.com/71215978/144743006-964e7b01-4406-4280-bdfe-fe9a56bd5402.png)

>### A. 프로젝트명
: Nagios를 이용한 모니터링 서비스
<br><br>


>### B. 프로젝트 멤버
* #### 이진우<br>
<t>1) web01에 was01의 OS 기본 구성<br>
<t>2) web01에 웹서버 및 mod_jk 설치<br>
<t>3) was01에 WAS 설치, DB connector 설치<br>
<t>4) mgt01에 nagios 패키지 설치<br>
<t>5) mgt01에 모니터링 구성<br>

* #### 이명주<br>
<t>1) 초기 VM 생성, OS 설치<br>
<t>2) dbm01과 mgt01의 OS 기본 구성<br>
<t>3) dbm01에 DB 설치<br>
<t>4) Web-WAS-DB 연동<br>
<t>5) web01,was01,dbm01에 nrpe 설치<br>
<t>6) web01,was01,dbm01에 모니터링 구성<br>
<t>7) Github 관리
<br><br>
  
  
>### C.	프로젝트 소개 및 개발 내용 소개
* #### Nagios<br>
: Nagios는 시스템 및 네트워크 모니터링 응용프로그램으로, 지정한 호스트와 서비스를 관찰하고 장애가 발생하거나 복구되었을 때 경보를 발령해준다. Nagios는 서버(nagios)와 클라이언트(nrpe) 방식으로 구현된다. 원래 Nagios는 Linux에서 실행되도록 디자인되어 졌음에도 불구하고 Linux 뿐만 아니라 Windows까지 모니터링 가능하며, 서버에서 발생하는 특정 상황을 정의하여 모니터링 할 수 있다.
  <br><br>

* #### Nagios의 기능<br>
  <t>1. 네트워크 서비스 모니터링(SMTP, POP3, HTTP, NNTP, PING, 등)<br>
  <t>2. 호스트 자원 모니터링(프로세서 부하, 디스크 사용량, 등)<br>
  <t>3. 자신들의 서비스 체크할 플러그인을 쉽게 개발할 수 있도록 한 간단한 플러그인 디자인<br>
  <t>4. 병렬화 된 서비스 체크<br>
  <t>5. 다운된 호스트와 통신 되지 않는 호스트의 탐지와 구분을 가능하게 하는 트리구조의 네트워크 호스트 구조정의 기능<br>
  <t>6. 서비스 또는 호스트의 문제가 발생하거나 해결되었을 때 통보(이메일, SMS, 사용자정의 방법)<br>
  <t>7. 서비스 또는 호스트 이벤트의 사전 문제 해결 시 실행될 이벤트 핸들러 정의기능<br>
  <t>8. 자동 로그 파일 순환<br>
  <t>9. 모니터링 호스트 이중화 지원<br>
  <t>10. 현재 네트워크 상태, 통보와 문제발생 이력, 로그 파일 등을 보기 위한 선택적 웹 인터페이스
  <br><br>
    
* #### 시스템 요구사항<br>
  : Nagios를 실행하는데 필요한 것은 리눅스(또는 Unix)가 깔린 장비와 C 컴파일러 뿐이다.<br> 
    네트웍을 통해 대부분의 서비스 체크가 수행되므로 TCP/IP를 설정 해야 할 것이다.<br>
    * 웹 서버(되도록이면 Apache)<br>
    * Thomas Boutell의 gd 라이브러리 1.6.3 이상 버전(statusmap과  trends CGIs에 필요)
    <br><br>
      
* #### NRPE<br>
 : NRPE(Nagios Remote Plugin Executor)는 원격 시스템에서 호스팅 되는 스크립트를 사용하여 원격 시스템 모니터링을 허용하는 Nagios 에이전트이다. 디스크 사용량, 시스템 부하 또는 현재 로그인한 사용자 수와 같은 리소스를 모니터링할 수 있다. Nagios는 check_nrpe플러그인을 사용하여 원격 시스템의 에이전트를 주기적으로 폴링한다.<br>
NRPE를 사용하면 다른 Linux/Unix 시스템에서 Nagios 플러그인을 원격으로 실행할 수 있다. 이를 통해 원격 시스템 메트릭(디스크 사용량, CPU 로드 등)을 모니터링할 수 있다. NRPE는 또한 일부 Windows 에이전트 추가 기능과 통신할 수 있으므로 원격 Windows 시스템에서도 스크립트를 실행하고 메트릭을 확인할 수 있다.
    <br><br>



>### D.	프로젝트 개발 결과물 소개
* #### Diagram
![Diagram](https://user-images.githubusercontent.com/71215978/142678872-50a4ab42-fedc-45a2-90cf-dc70230f6c91.png)
<br><br>
  
>### E.	개발 결과물을 사용하는 방법 소개 
<br><br>
  <img width="1294" alt="스크린샷 2021-12-05 오후 7 04 38" src="https://user-images.githubusercontent.com/66203627/144742202-2766ce89-706d-43ab-9797-0e40afea3dc5.png">
  <br><br>
* Nagios를 설치한 서버의 IP주소/nagios 로 이동하게 되면 아이디와 비밀번호를 입력하라는 창이 뜬다.<br>
  초기 아이디와 비밀번호인 nagiosadmin, nagiosadmin 을 입력하여 로그인하면 된다.
  <br><br>
  <img width="1294" alt="스크린샷 2021-12-05 오후 7 05 09" src="https://user-images.githubusercontent.com/66203627/144742239-aa4321ca-8b31-4815-8498-73f75184b61f.png">
  <br><br>
* 로그인하게 되면 위와 같은 페이지가 보여지게 된다.<br>
  현재 서비스로 등록된 가상머신을 모니터링 하기 위해서는 좌측에 있는 Services를 클릭 하여 이동한다.
  <br><br>
  <img width="1294" alt="스크린샷 2021-12-05 오후 7 08 08" src="https://user-images.githubusercontent.com/66203627/144742271-0a1ea9bf-274a-41c1-9e02-ee07af0d9ac3.png">
  <br><br>
* 이동하게 되면 위와 같은 페이지가 보여지게 된다.<br>
  등록한 가상머신의 현재 상태, Ping, SSH 등과 가상머신마다 다른 mariaDB, tomcat, httpd의 현재 상태를 모니터링 할 수 있다. 
  <br><br>
  
  

 
  

>### F.	개발 결과물의 필요성 및 활용방안<br>
*  리눅스 및 유닉스, 윈도우 서버를 비롯한 대부분의 시스템에 대한 모니터링 서비스를 제공할 뿐만 아니라 IP 주소로 접근 가능한 네트워크 장치에 대한 모니터링 서비스도 제공할 수 있    다. <br>
*  서버 시스템에 운영되는 다양한 어플리케이션도 제공한다. <br>
*  24시간 중단 없이 서버가 사용하는 자원들까지도 모니터링 할 수 있다. <br>
*  Nagios는 시스템 및 서비스에 대한 모니터링 도중 문제점을 발견할 경우 관리자에게 알려준다. <br>
*  관리자는 Nagios가 실시간으로 보내는 문제들을 신속하게 발견하고 수정하여 중단 없는 서비스를 클라이언트에게 제공할 수 있다. <br>
*  관리자는 Nagios가 제공하는 웹 인터페이스를 통해 Nagios가 제공하는 모든 기능을 편리하게 관리할 수 있다. <br>
