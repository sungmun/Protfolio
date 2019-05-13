# 강성문

프로젝트를 통한 공부를 지향하는 개발자입니다

## 이력

---

-   2014.03 ~ 2019.03 수원과학대학(컴퓨터정보과)
-   2017.07 ~ 2018.05 실시간 테트리스 대결
-   2017.10 네트워크 관리사 2급
-   2017.05 기술경진대회 - 우수
-   2017.07 졸업과제전 - 우수
-   2018.05 ~ 2018.09 게시판(JSP)
-   2018.05 기술경진대회 - 우수
-   2018.09 ~ 2018.10 게시판(Spring Boot)
-   2018.10 ~ 현재 Kakao-Clone(Web)

## 프로젝트 상세설명

---

### [실시간 테트리스 대결](https://github.com/sungmun/TetrisClient)

Java로 만든 첫번째 개인프로젝트로, Java의 Swing을 이용하여 GUI를 만들어 간단한 테트리스를 만드는 부분은 금방 만들었으나, MVC 디자인에대한 이해 부족으로 MVC 디자인을 적용하는것에 시간이 많이 걸리고, 소켓통신을 이용하여 대결 기능을 넣기위해, 대전기능뿐만 아니라 로그인부터 대기실까지 만드는데 시간이 많이 걸린작품이다. 그리고 이 프로젝트는 기능이 완성이 된뒤에도 Java를 공부를 하다가 새롭게 알게되는 지식들을 이용하여 코드리펙토링작업이 지속적으로 이루어졌다. 이 프로젝트를 진행하며, 소켓통신에 대한 이해가 높아졌으며, JSON포멧에 대해 이해를 하게 되었다. 또한 Maven을 이용한 라이브러리 추가에 대해 알게 되었으며, git을 통한 최초의 프로젝트이다.

### [게시판(JSP)](https://github.com/sungmun/NoticeBoard)

웹개발자를 목표로 하고 시작한 프로젝트로, 간단한 CRUD기능이 있는 게시판을 목표로 만들어졌다. 세션을 이용한 로그인기능 회원가입, 게시물작성, 댓글작성 등의 기능이 들어간 게시판

#### 구성

-   Back-end

    -   servlet
    -   mysql

-   Front-end

    -   JSTL
    -   JSP
    -   BootStrap

웹에대한 지식이 부족한 상태에서 만들다보니, 만드는데 시간이 오래걸렸다. 이 프로젝트를 진행하며, 웹서버의 특징을 알게되었으며, 서블릿이 어디에 사용되는지와 기본적인 웹의 구조에대해 이해를 하게 되었다.

### [게시판(Spring Boot)](https://github.com/sungmun/SpringBoot-NoticeBoard)

JSP로 만든 게시판을 Spring Boot를 이용하여 다시 만들어보는 프로젝트로 Spring Boot를 이해하기 위해 만들어보았다.

#### 구성

-   Back-end

    -   springboot
    -   mysql
    -   handlebar.java

-   Front-end

    -   foundation
    -   handlebar.js

#### Issue

-   Study
    -   blog : [스프링 부트로 웹서비스 출시하기 - jojoldu](https://jojoldu.tistory.com/250), [예제로 확인하는 handlebars.js 사용방법 감성프로그래밍](https://programmingsummaries.tistory.com/381), [프론트와 UI서버를 같은 템플릿으로 관리하는 법 - 티몬개발블로그](https://tmondev.blog.me/220398995882?Redirect=Log&from=postView)
-   Sprign Security
    -   기존에는 로그인여부를 세션을 통해 해결을 하였으나, 세션을 통해 해결을 하는경우 유저가 많아지면 세션만 관리하는 서버를 사용해야되고, 서버사이드의 부하가 많아진다는 점을 알게 되었으며, RestfulAPI에 대해 알게 되었다.
-   handlebar
    -   게시물페이지에서 댓글부분은 클라이언트사이드렌더링(이후 CSR)하고 게시물부분은 서버에서 렌더링하기 위해, handlebar.java를 이용하여 서버사이드 렌더링(이후 SSR)을 하였다.
-   library
    -   JPA: ObjectRelationalMapping(ORM)을 처음 사용해보았으며, 왜 사용하는지에 대해 이해를 하였다.

### [Kakao-Clone(web)](https://github.com/sungmun/Kakao-Clone)

이 프로젝트는 KakaoTalk를 웹에서 가능한 비슷하게 만드는 프로젝트이다

#### 구성

-   Back-end

    -   node.js
    -   express
    -   mocha
    -   sequelize
    -   mariadb

-   Front-end

    -   react.js
    -   redux

#### Issue

-   login

    -   로그인을 google과 facebook에서 제공하는 oauth 로그인을 이용하여 만들었으며, 최초 구현시에는 back-end에서 social서버로 데이터를 보내서 로그인을 하는 동작으로 구현을 했으나, 차후에 client에서 social서버로 데이터를 보내서 login정보를 받고 이정보를 서버에 보내서 그정보로 로그인을 하는 방식으로 변경

-   sequelize

    -   sequelize를 이용하여 db구성시 seqielize 공식 Document에 나오지 않는 부분이 많아 지체되는 부분이 많았으나, velog의 [@cadenzah](https://velog.io/@cadenzah)님의 _Sequelize 공식 Document 시리즈_ 를 보고 해결하였다

-   TDD

    -   TDD를 도입후 테스트를 진행할 때마다 DB의 데이터가 변경되는것이 싫어서 mock를 이용하여 DB의 변경을 최소화하였다.

-   style

    -   *ESLint*와 vscode의 플러그인 _Prettier_, Airbnb Style을 이용하여 자동으로 수정이 가능한 부분은 자동으로 수정을 하고 아닌부분은 직접적으로 수정을 하였다

-   React
    -   front-end부분의 개발은 두차례에 거쳐서 이루어 졌는데, 첫번째에는 한창 SSR에 알아보던 시기라 Next.js를 통해 SSR을 하였다. 그리고 두번째에 다시 생각을 해보니 이 프로젝트는 SSR이 필요없는 프로젝트라는 사실과 React에 새로 추가된 hooks이 매우 사용해보고 싶어 Next.js를 배제하고 hooks기능을 추가한 코드를 전체적으로 재작성하기로 하고 전체적으로 수정을 하였다.
