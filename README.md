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

#파일명: forward_date.jsp






