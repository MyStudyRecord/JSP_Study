# JSP-Study
정보처리기사 JSP 공부
<br><br>

### index.jsp
<b>전체적인 기본 틀(화면) 구성</b>
~~~
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

//top : 말 그대로 가장위에서 margin을 줘서 밀어내는 형식이다. 만약 header의 height가 40px이라면 section의 top을 40px을 주면 40px만큼 밀려 header바로 아래에 위치하게 된다
//position: fixed : 일단 위치를 고정한다
//width: 100% : 가로를 꽉 채운다
//height: 100% : 세로를 꽉 채운다
//text-align : 텍스트의 가로위치 설정
//line-height : 텍스트의 세로위치 설정
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
~~~

### header.jsp
<b>header부분을 쉽게 재사용하기 위해 만든 파일 <jsp:include page="header.jsp"/> 로 사용할 수 있다</b>
~~~
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
~~~

### footer.jsp
<b>footer부분을 쉽게 재사용하기 위해 만든 파일 <jsp:include page=".jsp"/> 로 사용할 수 있다</b>
~~~
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
~~~

### join.jsp
<b>join화면에 해당하는 jsp 파일</b>
~~~
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>join</title>
</head>
<body>
<script type="text/javascript" src="check.js"></script>

<jsp:include page="header.jsp"/>
<section style="position: fixed; top: 80px; width: 100%; height: 100%">
<h2 style="text-align: center">홈쇼핑 회원 등록</h2><br>

<form name="frm" style="display: flex; align-items: center; justify-content: center; text-align: center">
<table border="1">
<tr>
<td>회원번호(자동발생)</td>

//readonly="readonly" : 읽기만 가능하고 칸안에 입력 불가
<td><input type="text" name="custno" readonly="readonly"></td>
</tr>

<tr>
<td>회원성명</td>
<td><input type="text" name="custname"></td>
</tr>

<tr>
<td>회원전화</td>
<td><input type="text" name="phone"></td>
</tr>

<tr>
<td>회원주소</td>
<td><input type="text" name="address"></td>
</tr>

<tr>
<td>가입일자</td>
<td><input type="text" name="joindate"></td>
</tr>

<tr>
<td>고객등급[A: VIP, B:일반, C: 직원]</td>
<td><input type="text" name="grade"></td>
</tr>

<tr>
<td>도시코드</td>
<td><input type="text" name="city"></td>
</tr>

<tr>
<td colspan="2">
<input type="submit" value="등록" onclick="return joinCheck()"> &nbsp;
<input type="button" value="조회">
</td>
</tr>
</table>
</form>
</section>
<jsp:include page="footer.jsp"/>
</body>
</html>
~~~

### check.js
<b>예외처리를 할수 있는 파일이다, 예 : 입력해야하는 칸이 공백일 경우 공백이라고 경고 표시 <br> body 태그 아래에 선언해 사용할 수 있다 <script type="text/javascript" src="check.js"></script></b>
~~~
//alert : 안내문 표시
//form name.input name.focus(); : 지정한 위치로 커서 이동
//document.form name.input name.value.length == 0 : 공백인지 확인하는 코드

function joinCheck(){
	if(document.frm.custname.value.length == 0){
		alert("회원성명이 입력되지 않았습니다");
		frm.custname.focus();
		return false;
	}
	
		if(document.frm.phone.value.length == 0){
		alert("회원전화가 입력되지 않았습니다");
		frm.phone.focus();
		return false;
	}


	if(document.frm.address.value.length == 0){
		alert("회원주소가 입력되지 않았습니다");
		frm.address.focus();
		return false;
	}
	
	
	
		if(document.frm.joindate.value.length == 0){
		alert("가입일자가 입력되지 않았습니다");
		frm.joindate.focus();
		return false;
	}

	if(document.frm.grade.value.length == 0){
		alert("고객등급이 입력되지 않았습니다");
		frm.grade.focus();
		return false;
	}	
	
		if(document.frm.city.value.length == 0){
		alert("도시코드가 입력되지 않았습니다");
		frm.city.focus();
		return false;
	}
	
	success();
	return true;
}

function success(){
	alert("회원등록이 완료 되었습니다!");	
}
~~~
