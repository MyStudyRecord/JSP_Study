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
