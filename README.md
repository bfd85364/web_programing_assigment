# web_programing_assigment


#forward -second 
--파일명: second.jsp

<%@ page contentType="text/html; charset=utf-8" %>
<html>
<head>
  <title>Action Tag</title>
</head>
<body>
  <h3> 파일은 second.jsp입니다. </h3>
  today is: <%=new java.util.Date() %> 
</body>
</html>



# forward- 날짜
<%@ page contentType="text/htnml; charset=utf-8" %>
<html>
  <head>
    <title>Action Tag</title>
  </head>
  <body>
    <h2>forward 액션 태그</h2>
    <jsp:forward page="forward_date.jsp"/>
  </body>
</html>

-- 파일명: forward_date.jsp
<%@ page contentType="text/html; charset=utf-8" %>
<html>
  <head>
    <title>Action Tag</title>
  </head>
  <body>
    <p>오늘의 날짜 및 시간</p>
    <p><%=(new java.util.Date()).toLocaleString() %></p>
  </body>
</html>


#include 액션태그 사용 예 

<%@ page contentType="text/html; charset=utf-8" %>
<html>
  <head>
    <title>Action Tag</title>
  </head>
  <body>
    <h3>이 파일은 first.jsp입니다.</h3>
    <jsp:include page="second_2.jsp" flush="false"/>
    <p>Jakarta Server Page</p>
  </body>
</html>

<%@ page contentType="text/html; charset=utf-8"%>

-- 파일명: second_2.jsp





