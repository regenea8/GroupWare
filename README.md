# GroupWare
반응형 웹으로 제작한 그룹웨어 입니다.   
편지함,전자결재,일정관리,게시판,자료실 기능을 넣었습니다.  
개발환경은 다음과 같습니다.  

- Operating System : Windows 8.1 K
- Programming Language : JAVA (JDK1.8.0_65)
- DBMS : ORACLE
- Web Application Server : Tomcat 8.0
- 형상관리 : GitHub (https://github.com/regenea8/GroupWare)
- Framework : Spring 4.0, Mybatis 2.0, Bootstrap
- Technology : JDBC, HTML 5.0, CSS, Javascript, jQuery, ajax
- Tool : Eclipse (MARS1), eXERD, sqldevelopr  
- api : 다음 주소검색, 네이버 스마트에디터, jQuery EasyUI1.5.1, Viewr JS

# 설명

첫 로그인 화면 입니다.  
여기서는 사원번호와 비밀번호로 로그인을 합니다.  
다른 페이지를 들어가려고 해도 로그인이 되어있지 않으면 로그인 페이지로 리다이렉트 되도록 처리 하였습니다.  
로그인 하고 들어가면 첫 화면인 자유게시판으로 이동하게 됩니다.   
![1](https://user-images.githubusercontent.com/23238585/62043999-d7cf9c00-b23c-11e9-8630-16489811210c.jpg)

게시판의 종류는 3가지 입니다.   
자유게시판, 사내동호회, 중고장터가 있습니다.  
글 등록, 수정, 삭제를 할 수 있고 등록한 글을 작성자, 제목 으로 검색할 수 있습니다.  
![2](https://user-images.githubusercontent.com/23238585/62044000-d8683280-b23c-11e9-9a0d-1b4cde9b7db5.jpg)

네이버 스마트에디터 api 를 사용하여 게시판 글 작성하는 모습 입니다.  
![3](https://user-images.githubusercontent.com/23238585/62044001-d8683280-b23c-11e9-8cf7-7b9a6c41cb5c.jpg)

조회하면 다음과 같은 화면이 나옵니다.   
수정,삭제,목록 버튼이 있고, 밑에는 리플 추가,수정,삭제를 할 수 있습니다.  
![4](https://user-images.githubusercontent.com/23238585/62044002-d8683280-b23c-11e9-84cc-8f6c1626d1bb.jpg)

다음 사진은 자료실 조회한 모습 입니다.   
날짜 밑에 자료파일이름을 클릭하면  업로드한 파일을 다운로드 받을 수 있습니다.  
![5](https://user-images.githubusercontent.com/23238585/62044003-d8683280-b23c-11e9-8aca-4f2d97a4cd26.jpg)

다음은 편지함 입니다. 받은 편지함에서 편지쓰기 버튼을 누르면 모달창이 나옵니다.    
제목,내용, 받은사원번호,파일 첨부하고 확인 버튼을 누르면 편지가 전송 됩니다.  
![6](https://user-images.githubusercontent.com/23238585/62044004-d900c900-b23c-11e9-8b9d-84f5d353ef84.jpg)

다음 사진은 받은사람 아이디로 로그인 하여 들어온 모습입니다.  
방금 보낸 편지가 도착해 있습니다.  
![7](https://user-images.githubusercontent.com/23238585/62044005-d900c900-b23c-11e9-809d-e7b5930fd3d6.jpg)

조회 버튼을 누르면 받은 편지 내용을 확인 할 수 있고 첨부파일을 받을수 있습니다.  
![8](https://user-images.githubusercontent.com/23238585/62044006-d900c900-b23c-11e9-89d6-3fd84b6bce48.jpg)

보낸편지함에서 자기가 보낸 편지를 확인하거나  
![9](https://user-images.githubusercontent.com/23238585/62044007-d900c900-b23c-11e9-905c-20f92f39ec95.jpg)

받은편지함에서 편지를 선택하고 보관하기 버튼을 눌러 편지를 보관할 수 있습니다.  
![10](https://user-images.githubusercontent.com/23238585/62044009-d9995f80-b23c-11e9-9736-23d6123d4f64.jpg)

다음 화면은 전자결재 화면입니다.   
전자결재는 업무, 파견, 경비지출, 초과근무, 휴가 총 5가지가 있습니다.   
![11](https://user-images.githubusercontent.com/23238585/62044010-d9995f80-b23c-11e9-9775-3de2f1609afa.jpg)

모달창을 이용해서 전자결재 등록을 할 수 있습니다.
제목, 결재구분, 중간승인자 번호, 결재파일업로드 쓰고 입력버튼을 누릅니다. 
![12](https://user-images.githubusercontent.com/23238585/62044011-d9995f80-b23c-11e9-97f7-0eef676737d9.jpg)

중간승인자 번호로 로그인 하여 전자결재 리스트에 도착해있는 결재를 클릭합니다.  
그러면 조회 모달이 실행되고, 사원이 첨부하여 보낸 pdf 파일을 Viewer JS api 를 사용하여 만든 뷰어가 실행됩니다.  
중간관리자는 뷰어를 통해서 업무결재 내용을 확인하고 거절할지 승인할지 를 선택합니다.  
거절을 누르면 사원의 전자결재 리스트에서 거절로 나오고 승인을 누를경우 사원의 전자결재 내역에서는 승인(중간) 으로 표기가 되고 결재내역은 다시 최종결재자에게로 넘어가게 됩니다.  
![13](https://user-images.githubusercontent.com/23238585/62044012-d9995f80-b23c-11e9-9d89-28edffcdde37.jpg)

최종결재자의 화면입니다.. 마찬가지로 뷰어를 통해서 pdf 내용을 확인하고 거절과 승인 중 하나를 선택할 수 있습니다.   
여기서 승인을 할 경우 사원의 전자결재 리스트에는 승인(최종) 이라는 단어가 나오게 됩니다.  
![14](https://user-images.githubusercontent.com/23238585/62044014-da31f600-b23c-11e9-9f2f-3e06c8b1595c.jpg)

다음 사진은 일정관리에 들어온 모습 입니다.  
좌측 화면은 일정을 등록할 수 있는 입력폼 입니다.  
일정제목,시작일,종료일,내용을 입력하고 등록 버튼을 누르면 좌측 달력에 파란색 줄안에 일정 제목이 들어가게 됩니다.  
시작일,종료일을 이용하여 기간을 정하면 그만큼 일정내용이 들어가게 됩니다.  
또 같은날짜에 여러가지 일정이 들어가면 밑으로 추가 되게끔 되어있고 3개 이상 넘어가면 +2more 처럼 표시가 됩니다.  
그 표시를 누르게 되면 숨겨져 있던 일정이 보여지게 됩니다.  
![15](https://user-images.githubusercontent.com/23238585/62044016-da31f600-b23c-11e9-828e-596f0a0516ff.jpg)
![15-1](https://user-images.githubusercontent.com/23238585/62044017-da31f600-b23c-11e9-8c14-2c9134217906.jpg)

다음은 달력에 파란색 칸의 일정 제목을 클릭하면 나오는 일정조회 입니다.  
모달창에 상세조회 내용들이 나오고 있습니다.  
사내 일정이기 때문에 로그인 한 사원이 수정,삭제를 할 수 없지만 개인 일정에서는 수정 삭제가 가능 합니다.  
![16](https://user-images.githubusercontent.com/23238585/62044018-da31f600-b23c-11e9-8ebb-bf1be50b05b6.jpg)

관리자 아이디가 아닌경우 관리자 메뉴를 클릭하면 접근할 수 없다는 alert 창이 나옵니다.  
![17](https://user-images.githubusercontent.com/23238585/62044019-daca8c80-b23c-11e9-8570-33c9a796f96d.jpg)

여기서는 새로운 사원을 등록할 수 있습니다.  
관리자 구성원관리 탭에서 구성원 등록 버튼을 눌러서 다음과 같은 인적사항들을 입력합니다.  
비밀번호를 두번입력하여 두개의 비밀번호가 같아야만 처리가 되도록 하였고, 사원번호도 입력후 중복확인 버튼을 통하여 확인할 수 있도록 하였습니다.  
![18](https://user-images.githubusercontent.com/23238585/62044020-daca8c80-b23c-11e9-84cb-c8a3a02aef7b.jpg)

다음 주소검색 api 적용하여 주소를 쉽게 찾고 입력할 수 있도록 하였습니다.  
![19](https://user-images.githubusercontent.com/23238585/62044021-daca8c80-b23c-11e9-9252-6305ed0c5264.jpg)

사원의 내역을 다음과 같이 볼 수 있고 정보를 수정할 수 있습니다.  
좌측의 조직도에서는 EasyUI jQuery api 를 사용하여 부서별로 사원의 현황을 보기 쉽게 하였습니다.  
![20](https://user-images.githubusercontent.com/23238585/62044023-daca8c80-b23c-11e9-9721-c5f91714364a.jpg)

우측 위의 관리버튼을 누르면 조직관리 모달창이 나옵니다.  
여기서 부서명을 수정하거나 새로운 부서를 추가 할 수 있습니다.  
![20-1](https://user-images.githubusercontent.com/23238585/62044024-db632300-b23c-11e9-96cd-5c9659260598.jpg)

부서명을 더블클릭 하면 input 창으로 바뀌고 부서명을 바꾸고 수정버튼을 누르면 부서명이 수정 됩니다.  
![20-2](https://user-images.githubusercontent.com/23238585/62044026-db632300-b23c-11e9-9895-4fa95c7990dc.jpg)
![20-3](https://user-images.githubusercontent.com/23238585/62044028-db632300-b23c-11e9-8a13-7a6841a5cc8b.jpg)

마지막으로 해당 프로젝트의 ERD 입니다.  
끝까지 읽어주셔서 대단히 감사합니다.  
![21](https://user-images.githubusercontent.com/23238585/62044029-db632300-b23c-11e9-831a-2b2b5eb1a4da.png)
