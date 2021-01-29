# ✈️ Euroverse    
유로버스(여행 플래너 및 커뮤니티 사이트)는 국비학원에서 진행한 팀프로젝트입니다. (사이트 바로가기>>[Euroverse](http://13.125.136.145:8080/))
  ###### <p align="center"><img src = "https://ifh.cc/g/EkHN2E.jpg" width="500px">   **[사진1] 메인화면**   </p>
  
- - -  
# :blue_book: 목차
  ###     1 개요
  ###     2 담당 모듈
  ###     3 의존성 및 버전 정보
  ###     4 분석 및 설계 과정
  ###     5 추가 학습
  ###     6 참고 사항

- - -

## :one: 개요 
+ 총 개발 기간 : 2개월  
    + 분석 및 설계 : 2020/01/01 ~ 2020/01/23  
    + 구현 : 2020/01/24 ~ 2020/03/07  
+ 총 개발 인원 : 6명  
+ 시스템 개요 : MVC2 모델을 기반으로 스프링 프레임워크를 이용하여 만든 유럽 여행 플래너 및 커뮤니티 사이트입니다. 크게 회원 관리, 주문 관리, 플래너, 커뮤니티, 채팅 및 알람 모듈로 구성되어 있습니다.

## :two: 담당 모듈🌟

**1. 커뮤니티**  
  + 기능 : 커뮤니티 카테고리 별 게시글 조회, 작성, 수정, 삭제가 가능하며 게시글 좋아요, 북마크, 신고하기, 태그, 이전글/다음글 조회 가능
  + 설명
    - 게시글 작성시 **썸머노트**를 사용하여 작성
    - 게시글 북마크시 회원의 마이페이지에서 조회 가능
    - 게시글 작성시 태그 작성 가능 중복 태그는 불가하며 게시글 조회 화면에서 태그 클릭시 동일한 태그를 입력한 게시글 리스트로 이동
    - QnA 게시판은 전체, 루트, 도시, 교통, 숙소, 쇼핑/경비/환전, 기타 별로 게시글 분류
    
   ######  <p align="center"><img src="https://ifh.cc/g/vyrGVR.png" width=200> **[사진2] 알림 내역 조회** </p>
   
   **1-1. 회원이 작성한 플래너를 공유하는 플래너공유 게시판**
   + 기능 : 작성한 플래너를 플래너공유 게시판에 등록할 수 있고 등록된 플래너들은 다른 회원들이 본인의 플래너로 내려받기 가능
   + 설명
     - 플래너 조회 페이지에서 바로 공유가 가능하며 클릭시 플래너공유 게시판 작성하기 페이지로 이동
     - 작성하기 페이지에서 회원이 등록한 플래너들을 리스트로 보여주며 선택등록 가능
     
   ######  <p align="center"><img src="https://ifh.cc/g/RayOle.png" width=200> **[사진3] 플래너 채팅** </p>
   
   **1-2. 댓글과 대댓글**
   + 기능 : 게시글에 댓글/대댓글 작성 가능
   + 설명
     - 댓글/대댓글 작성, 수정, 삭제 가능하며 비밀글 설정시 댓글/대댓글 작성자와 게시글 작성자에게만 공개
     - 신고하기와 좋아요, 좋아요 취소 가능
     - 대댓글이 달렸는데 댓글 삭제시 "삭제된 댓글입니다" 문구로 변경되고 대댓글 작성 불가
     
   ######  <p align="center"><img src="https://ifh.cc/g/RayOle.png" width=200> **[사진3] 플래너 채팅** </p> 

**2. 동행**
  + 기능 :
  + 설명
    - 
    
   ######  <p align="center"><img src="https://ifh.cc/g/JKF59Y.png" width=200>**[사진4] 동행 채팅방 목록**  <img src="https://ifh.cc/g/WSks7r.png" width=200> **[사진5] 동행 채팅방 화면**  </p>
    
<!--사진 유효기간 : 200일  (만료 : 2021-08-10)-->

## :three: 의존성 및 버전 정보
  
+ Laguage : Java    
+ Back-end : Spring Framework 4.0.1 / MyBatis / Apache Tomcat / Selenium
+ Front : HTML5 / BootStrap 4 / CSS3 / jQuery / Ajax / JSP
+ Database : Oracle 10g / MongoDB 3.6.1  
+ VCS tool : GitHub  
+ IDE : Eclipse  
+ Open Source : Sweetalert / FullCalendar / SummerNote / Owl carousel / AOS / Swiper / Foreign exchange rates API / 공공데이터포털API / 청기와 LAB / I'mPort API / JavaMail API / 네이버로그인 API / 카카오로그인 API / GoogleMap API

## :four: 분석 및 설계 과정

    1. 주제 선정

    2.1. 업무 분석 : Use Case Modeling
        2.1.1 현업 요구사항 정의서 작성  
        2.1.2 요구사항 추적표 작성
        2.1.3 Use Case 유형정의 작성    
        2.1.4 Use Case Diagram 작성    
        2.1.5 Use Case 정의서 작성
    
    2.2. 업무 분석 : Application Modeling
        2.2.1 Class Diagram 작성    
        2.2.2 VOPC(View Of Participating Class) Diagram 작성

    2.3. 화면 분석
        2.3.1 화면 정의서 작성

    2.4. 데이터 분석(Logical)
        2.4.1 ERD(Logical) 작성
        
    3.1 업무 분석 : Application Modeling 
        3.1.1 설계표준 정의
        3.1.2 Class Diagram 작성
        3.1.3 VOPC(View Of Participating Class) Diagram 작성

    3.2 화면 분석
        3.2.1 화면 정의서 

    3.3 데이터 분석(Physical)
        3.3.1 ERD(Physical) 작성
        3.3.2 테이블 목록 작성
        3.3.3 테이블 정의서 작성

## :five: 추가 학습

### **⚡️ AWS 이용한 배포 [(Euroverse 바로가기)](http://13.125.136.145:8080/)**  
학원 수료 후 AWS를 이용해 배포를 해보았습니다. 아마존 **EC2**의 **인스턴스**를 2개 생성하여 각각 **웹 서버와 MongoDB**를 설치하였고, 아마존 **RDS**를 이용하여 Oracle 12를 설정했습니다. 각 인스턴스끼리 연동을 한 뒤 **탄력적 IP**를 생성하여 고정 IPv4 주소를 연결했습니다. 현재(2020/04/24) 셀레늄 구동을 완성하지 못해 항공권 검색과 숙소 검색 기능은 작동하지 않습니다.
  
## :six: 참고 사항  

**프로젝트 발표 영상(썸네일 클릭 시 이동)**

[![](https://img.youtube.com/vi/xGH5Dzj8rAY/mqdefault.jpg)](https://youtu.be/xGH5Dzj8rAY)

