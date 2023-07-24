# 2. jsp 파일 이용하기

----------------------------
## 목차

### [1. 의존성 설치](#1-의존성-설치-1)
### [2. jsp 파일 실행하도록 경로 설정](#2-jsp-파일-실행하도록-경로-설정-1)
### [3. jsp 파일을 넣을 폴더 생성](#3-jsp-파일을-넣을-폴더-생성-1)
### [4. url 경로에 따라 보여줄 페이지를 지정하는 컨트롤러 추가](#4-url-경로에-따라-보여줄-페이지를-지정하는-컨트롤러-추가-1)
### [5. jsp 한글 깨짐 해결하기](#5-jsp-한글-깨짐-해결하기-1)
### [6. jsp 파일에 jstl 라이브러리 적용하기](#6-jsp-파일에-jstl-라이브러리-적용하기-1)
### [7.jstl이란](#7-jstl이란-1)

----------------------------

### 1. 의존성 설치

- 의존성 추가
  - tomcat-embed-jasper는 스프링 부트에서 jsp 기능을 사용할 수 있도록 도와 줌
```
/pom.xml

...
<dependencies>
  <dependency>
    	<groupId>org.apache.tomcat.embed</groupId>
			<artifactId>tomcat-embed-jasper</artifactId>
			<scope>provided</scope>
  </dependency>
</dependencies>
```
<br />

- 의존성 추가 후 라이브러리 재설치
  - pom.xml 있는 위치에서 터미널에 입력
```
mvn clean install
```

------------------------------------------------

<br />

### 2. jsp 파일 실행하도록 경로 설정

```
/src/main/resources/application.properties

spring.mvc.view.prefix=/WEB-INF/view/
spring.mvc.view.suffix=.jsp

```

<br />

------------------------------------

<br />

### 3. jsp 파일을 넣을 폴더 생성

- src/main/webapp/WEB-INF/view 폴더 생성
- jsp 파일은 모두 view 폴더 안에 넣을 것
```
src/main/webapp/WEB-INF/view/

<%@ page language="java" contentType="text/html; charset=UTF-8"
pageEncoding="UTF-8"%>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    home입니다.
  </body>
</html>
```
<br />

------------------------------------------------
<br />

### 4. url 경로에 따라 보여줄 페이지를 지정하는 컨트롤러 추가

- 각 페이지에 해당하는 컨트롤러를 생성  
- return 값은 view의 파일명을 써주면 자동으로 연결  

```
src/main/java/com/board_springboot/controller/HelloController.java

package com.example.board_springboot.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {
    @RequestMapping("/")
    public String home () {
        return "home";
    }
}
```

------------------------------------------------
<br />

### 5. jsp 한글 깨짐 해결하기

- jsp 파일 상단에 코드 추가

```

<!-- 한글 깨지는 상황 해결  -->
<%@ page language="java" contentType="text/html; charset=UTF-8"
pageEncoding="UTF-8"%>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    home 입니다.
  </body>
</html>

```

------------------------------------------------
<br />

### 6. jsp 파일에 jstl 라이브러리 적용하기

- 의존성 추가
```
<dependency>
  <groupId>jakarta.servlet.jsp.jstl</groupId>
  <artifactId>jakarta.servlet.jsp.jstl-api</artifactId>
  <version>3.0.0</version>
</dependency>
<dependency>
  <groupId>jakarta.servlet</groupId>
  <artifactId>jakarta.servlet-api</artifactId>
  <version>6.0.0</version>
  <scope>provided</scope>
</dependency>
<dependency>
  <groupId>org.glassfish.web</groupId>
  <artifactId>jakarta.servlet.jsp.jstl</artifactId>
  <version>3.0.1</version>
</dependency>
```
- jstl 사용 코드 추가

```
<!-- jstl1 사용하기 위해 추가 -->
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<!-- 한글 깨지는 상황 해결  -->
<%@ page language="java" contentType="text/html; charset=UTF-8"
pageEncoding="UTF-8"%>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    home 입니다.
  </body>
</html>
```

### 7.jstl이란

- jsp 내에서 자주 사용되는 반복문, 조건문 등의 로직을 쉽게 처리하기 위한 태그 라이브러리
