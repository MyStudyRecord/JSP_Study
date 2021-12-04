# JSP-Study
정보처리기사 JSP 공부
<br><br>

### index.jsp
<b>전체적인 기본 틀(화면) 구성</b>
~~~
<pre><code>
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>index</title>
</head>
<body>
<jsp:include page="header.jsp"/>
<section style="position: fixed; top: 80px; width: 100%; height: 100%">
<h2 style="text-align: center">쇼핑몰 회원관리 프로그램 </h2> <br>
<p style="padding-left: 10px">쇼핑몰 회ㅜ언정보왈머ㅣㅁㄷㄹ<br>
프로그램 작성순서<br>
1.ㅁㄻㄻ<br>
2.ㅎㄱㅁㄷㅎ<br>
3.ㄻㄻㄹ
</p>
</section>
<jsp:include page="footer.jsp"/>
</body>
</html>
</code></pre>
~~~

### header.jsp
<b>header부분을 쉽게 재사용하기 위해 만든 파일 <jsp:include page="header.jsp"/> 로 사용할 수 있다</b>
~~~
<pre><code>
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>header</title>
</head>
<body>
<header style="position: fixed; background-color: blue; color: white; top: 0px; width: 100%; height: 50px; text-align: center; line-height: 50px">쇼핑몰 관리 ver1.0</header>
<nav style="background-color: lightblue; color: white; width: 100%; position: fixed; line-height: 30px; height: 30px; top: 50px; padding-left: 20px">회원등록&nbsp;회원목록조회/수정 &nbsp;회원매출조회 &nbsp;홈으로</nav>
</body>
</html>
</code></pre>
~~~

### footer.jsp
<b>footer부분을 쉽게 재사용하기 위해 만든 파일 <jsp:include page=".jsp"/> 로 사용할 수 있다</b>
~~~
<pre><code>
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>footer</title>
</head>
<body>
<footer style="position: fixed; bottom: 0px; width: 100%; height: 30px; background-color: blue; color: white; text-align: center; line-height: 30px"> HRDKOREA Copyright ⓒ 어쩌고 저쩌고~</footer>
</body>
</html>
</code></pre>
~~~
