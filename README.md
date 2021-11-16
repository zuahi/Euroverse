# ✈️ Euroverse    
유로버스(여행 플래너 및 커뮤니티 사이트)는 국비학원에서 진행한 팀프로젝트입니다.

  ###### [<p align="center"><img src="https://user-images.githubusercontent.com/57661445/142063613-37302fd2-249f-4a6d-9635-d8894960af5e.png" width="400px">](http://13.125.136.145:8080/)  << 로고 클릭시 홈페이지로 이동</p>
  
- - -  

# :blue_book: 목차
  ###     1. 개요
  ###     2. 담당 모듈
  ###     3. 의존성 및 버전 정보
  ###     4. 분석 및 설계 과정
  ###     5. 추가 학습
  ###     6. 참고 사항

- - -

## 1. 개요 
+ 총 개발 기간 : 2개월  
    + 분석 및 설계 : 2020/01/01 ~ 2020/01/23  
    + 구현 : 2020/01/24 ~ 2020/03/07  
+ 총 개발 인원 : 6명  
+ 시스템 개요 : MVC2 모델을 기반으로 스프링 프레임워크를 이용하여 만든 유럽 여행 플래너 및 커뮤니티 사이트입니다. 크게 회원 관리, 주문 관리, 플래너, 커뮤니티, 채팅 및 알람 모듈로 구성되어 있습니다.

## 2. 담당 모듈

**1. 커뮤니티**  
  + 기능 : 커뮤니티 카테고리(인기글게시판/플래너공유/여행후기/여행정보/QnA/자유게시판) 별 게시글 조회, 작성, 수정, 삭제가 가능하며 게시글 좋아요, 북마크, 신고하기, 태그, 이전글/다음글 조회 가능
  + 설명
    - 게시글 작성시 **썸머노트**를 사용하여 작성
    - 게시글 작성시 태그 작성 가능 중복 태그는 불가하며 게시글 조회 화면에서 태그 클릭시 동일한 태그를 입력한 게시글 리스트로 이동
    - 게시글 작성시 관리자는 공지사항으로 등록 가능
    - QnA 게시판은 전체, 루트, 도시, 교통, 숙소, 쇼핑/경비/환전, 기타 별로 게시글 분류
    - 인기글게시판은 **스프링 스케쥴러**를 사용하여 일간/주간/월간별로 리셋후 조회수가 높은 순으로 등록  

   **<자유게시판 목록>**
   ![스크린샷(23)](https://user-images.githubusercontent.com/57661445/106381180-55f49c00-63fa-11eb-9b8a-8a1cc7c68677.png)
   
   **<게시글 조회>**
   ![스크린샷(24)](https://user-images.githubusercontent.com/57661445/106380887-8fc4a300-63f8-11eb-85d4-876abc1bcf23.png)
   
   
   
   **1-1. 회원이 작성한 플래너를 공유하는 플래너공유 게시판**
   + 기능 : 작성한 플래너를 플래너공유 게시판에 등록할 수 있고 등록된 플래너들은 다른 회원들이 본인의 플래너로 내려받기 가능
   + 설명
     - 플래너 조회 페이지에서 바로 공유가 가능하며 클릭시 플래너공유 게시판 작성하기 페이지로 이동
     - 작성하기 페이지에서 회원이 등록한 플래너들을 리스트로 보여주며 선택등록 가능
     
   **<플래너 공유 게시판 목록>**
   ![스크린샷(25)](https://user-images.githubusercontent.com/57661445/106380897-95ba8400-63f8-11eb-8cef-ac02ba89c587.png)
   
   
   
   **1-2. 댓글과 대댓글**
   + 기능 : 게시글에 댓글/대댓글 작성 가능
   + 설명
     - 댓글/대댓글 작성, 수정, 삭제 가능하며 비밀글 설정시 댓글/대댓글 작성자와 게시글 작성자에게만 공개
     - 신고하기와 좋아요, 좋아요 취소 가능
     - 대댓글이 달렸는데 댓글 삭제시 "삭제된 댓글입니다" 문구로 변경되고 대댓글 작성 불가

   **<댓글/대댓글 목록>**
   ![스크린샷(26)](https://user-images.githubusercontent.com/57661445/106380898-96ebb100-63f8-11eb-8268-cfdae47a3fc0.png)



**2. 동행**
  + 기능 : 제목, 동행시작일, 동행종료일, 인원, 내용, 태그를 입력 후 게시글을 등록 회원들은 동행 참여 메세지를 보낼 수 있고 동행에 참여한 회원들의 목록이 게시글에 나타남
  + 설명
    - 동행 게시글 작성과 조회는 본인인증 회원만 가능
    - 동행 참여자들의 프로필 사진, 닉네임, 여행스타일 목록과 참여자 수, 채팅방개설 버튼, 동행신청 버튼이 게시글에 나타남 동행에 참여중일 경우 탈퇴하기 버튼 생성
    - 이미 동행을 신청하였거나 동행인원이 다 찼을경우 동행신청 불가
    - 동행인원이 2명 이상일 경우 채팅방개설 버튼 생성
    - 동행신청 버튼 클릭시 동행 게시글 작성자에게 메세지를 작성하여 신청 가능

   **<동행찾기 게시글>**
   ![스크린샷(27)](https://user-images.githubusercontent.com/57661445/106380889-92bf9380-63f8-11eb-8e73-9015d572a4a7.png)
   
   **<동행신청 모달>**
   ![스크린샷(28)](https://user-images.githubusercontent.com/57661445/106380890-92bf9380-63f8-11eb-8c00-4e5fdd32f57b.png)
    
    
    
   **2-1. 참여중인 동행**
   + 기능 : 현재 참여중인 동행 목록을 보여주며 탈퇴하기 가능
   + 설명
     - 현재 참여중인 동행 목록을 동행 게시글 제목, 회원들의 프로필 사진, 닉네임, 여행스타일과 함께 보여주며 목록에서 탈퇴하기버튼 클릭시 동행 목록에서 사라지며 참여자 명단에서 제외
     
   **<참여중인 동행 목록>**
   ![스크린샷(30)](https://user-images.githubusercontent.com/57661445/106380893-93f0c080-63f8-11eb-9135-bb882e11ad7b.png)
     
     
     
   **2-2. 신청받은 동행, 요청한 동행**
   + 기능 : 회원이 작성한 게시글에서 신청받은 동행 목록을 보여주는 신청받은 동행과 동행신청한 제안 목록을 보여주는 요청한 동행
   + 설명
     - 게시글 제목, 동행 신청한 회원의 닉네임, 동행신청 메세지, 동행신청 날짜 표시
     - (신청받은 동행) 수락버튼 클릭시 동행에 참여되며 동행 목록이 보여지고 거절버튼 클릭시 신청받은 동행 목록에서 제거
     - (요청한 동행) 게시글 작성자가 동행 수락/거절 버튼 클릭시 요청한 동행 목록에서 제거 
    
   **<신청받은 동행 목록>**
   ![스크린샷(32)](https://user-images.githubusercontent.com/57661445/106380894-9521ed80-63f8-11eb-9df8-68bfdf543e6f.png)
   
   **<요청한 동행 목록>**
   ![스크린샷(29)](https://user-images.githubusercontent.com/57661445/106381334-53467680-63fb-11eb-8b67-c6cd6e5cecbf.png)
    
    
    
## 3. 의존성 및 버전 정보
  
+ Laguage : Java    
+ Back-end : Spring Framework 4.0.1 / MyBatis / Apache Tomcat / Selenium
+ Front : HTML5 / BootStrap 4 / CSS3 / jQuery / Ajax / JSP
+ Database : Oracle 10g / MongoDB 3.6.1  
+ VCS tool : GitHub  
+ IDE : Eclipse  
+ Open Source : Sweetalert / FullCalendar / SummerNote / Owl carousel / AOS / Swiper / Foreign exchange rates API / 공공데이터포털API / 청기와 LAB / I'mPort API / JavaMail API / 네이버로그인 API / 카카오로그인 API / GoogleMap API

## 4. 분석 및 설계 과정

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

## 5. 추가 학습

### **⚡️ AWS 이용한 배포 [(Euroverse 바로가기)](http://13.125.136.145:8080/)**  
학원 수료 후 AWS를 이용해 배포를 해보았습니다. 아마존 **EC2**의 **인스턴스**를 2개 생성하여 각각 **웹 서버와 MongoDB**를 설치하였고, 아마존 **RDS**를 이용하여 Oracle 12를 설정했습니다. 각 인스턴스끼리 연동을 한 뒤 **탄력적 IP**를 생성하여 고정 IPv4 주소를 연결했습니다. 셀레늄 구동을 완성하지 못해 항공권 검색과 숙소 검색 기능은 작동하지 않습니다.
  
## 6. 참고 사항  

**프로젝트 발표 영상(썸네일 클릭 시 이동)**

[![](https://img.youtube.com/vi/xGH5Dzj8rAY/mqdefault.jpg)](https://youtu.be/xGH5Dzj8rAY)

