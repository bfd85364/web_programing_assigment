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

# 파일명: forward_date.jsp
<%@ page contentType="text/html; charset=utf-8" %>
<html>
  <head>
    <title>Action Tag</title>
  </head>
  <body>
    <p>오늘의 날짜 및 시간</p>
    <p><%=(new java.util.Date()).toLocaleString() %>
  </body>
</html>


# include 액션태그 사용 예 

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

# 파일명: second_2.jsp

<%@ page contentType="text/html; charset=utf-8"%>
<html>
<head>
  <title>Action Tag</title>
</head>
<body>
  <h3>이  파일은 second_2.jsp입니다.</h3>
  Today is: <%=new java.util.Date() %> 
</body>
</html>

# include 액션태그 현재날짜 및 시간 출력 

<%@ page contentType="text/html; charset=utf-8 %">
<html>
<head>
<title>Action Tag</title>
</head>
<body>
  <p>오늘의 날짜 및 시각</p>
  <p><%=(new java.util.Date()).toLocaleString() %>
</body>
</html>

# Forward 액션태그와 param 액션태그

<%@ page contentType="text/html; charset=utf-8" %>
<html>
  <head>
    <title>Action Tag</title>
  </head>
  <body>
    <h3>param 액션 태그</h3>
    <jsp:forward page="param01_data.jsp">
      <jsp:param name="id" value="admin"/>
      <jsp:param name="name" value='<%=java.net.URLEncoder.encode("관리          자")%>'/>
    </jsp:param>
    <p>Jakarta Server Page
  </body>
</html>

# 파일명: param01_data.jsp
<%@ page contentType="text/html; charset=utf-8" %>
<html>
  <head>
    <title>Action Tag</title>
  </head>
  <body>
      <p> 아이디: <%=request.getParameter("id") %>
        <% 
          String name=request.getParameter("name");
        %>
      <p> 이름 <%=java.net.URLDecoder.decode(name) %>
  </body>
</html>




