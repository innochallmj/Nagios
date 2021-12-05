# NagiosMonitoring Project


>### A. 프로젝트명
: Nagios를 이용한 모니터링 서비스
<br><br>


>### B. 프로젝트 멤버
* 이진우<br>
<t>1) web01에 was01의 OS 기본 구성<br>
<t>2) web01에 웹서버 및 mod_jk 설치<br>
<t>3) was01에 WAS 설치, DB connector 설치<br>
<t>4) mgt01에 nagios 패키지 설치<br>
<t>5) mgt01에 모니터링 구성<br>

* 이명주<br>
<t>1) 초기 VM 생성, OS 설치<br>
<t>2) dbm01과 mgt01의 OS 기본 구성<br>
<t>3) dbm01에 DB 설치<br>
<t>4) Web-WAS-DB 연동<br>
<t>5) web01,was01,dbm01에 nrpe 설치<br>
<t>6) web01,was01,dbm01에 모니터링 구성<br>
<t>7) Github 관리
<br><br>
  
  
>### C.	프로젝트 소개 및 개발 내용 소개
* Nagios<br>
: Nagios는 시스템 및 네트워크 모니터링 응용프로그램으로, 지정한 호스트와 서비스를 관찰하고 장애가 발생하거나 복구되었을 때 경보를 발령해준다. Nagios는 원래 Linux에서 실행되도록 디자   인되어 졌음에도 불구하고 대부분의 다른 유닉스에서도 잘 작동한다.
  <br><br>

>### D.	프로젝트 개발 결과물 소개
* Diagram
![Diagram](https://user-images.githubusercontent.com/71215978/142678872-50a4ab42-fedc-45a2-90cf-dc70230f6c91.png)
<br><br>
  
>### E.	개발 결과물을 사용하는 방법 소개 
<br><br>
  

>### F.	개발 결과물의 필요성 및 활용방안<br>
  <t>1) 리눅스 및 유닉스, 윈도우 서버를 비롯한 대부분의 시스템에 대한 모니터링 서비스를 제공할 뿐만 아니라 IP 주소로 접근 가능한 네트워크 장치에 대한 모니터링 서비스도 제공할 수 있    다. <br>
  <t>2) 서버 시스템에 운영되는 다양한 어플리케이션도 제공한다. <br>
  <t>3) 24시간 중단 없이 서버가 사용하는 자원들까지도 모니터링 할 수 있다. <br>
  <t>4) Nagios는 시스템 및 서비스에 대한 모니터링 도중 문제점을 발견할 경우 관리자에게 알려준다. <br>
  <t>5) 관리자는 Nagios가 실시간으로 보내는 문제들을 신속하게 발견하고 수정하여 중단 없는 서비스를 클라이언트에게 제공할 수 있다. <br>
  <t>6) 관리자는 Nagios가 제공하는 웹 인터페이스를 통해 Nagios가 제공하는 모든 기능을 편리하게 관리할 수 있다. <br>
