# 1. 스프링 부트 설치하기

## 목차

### [1. 설치 환경](#1-설치-환경-1)
### [2. vs code 익스텐션 설치하기](#2-vs-code-익스텐션-설치하기-1)
### [3. 스프링 부트 프로젝트 만들기](#3-스프링-부트-프로젝트-만들기-1)
### [4. Gradle과 Maven의 차이](#4-gradle과-maven의-차이-1)
### [5. Jar, War의 차이](#5-jar-war의-차이-1)
### [6. 과정 진행 후 폴더 구조](#6-과정-진행-후-폴더-구조-1)

----------------------------------

### 1. 설치 환경

-  windows 10
-  vs code
-  java 17

----------------------------------

### 2. vs code 익스텐션 설치하기

- Extemsopm Pack for Java  
  자바 언어 자동완성 등 편이성 제공.
  <br></br>
- Spring Boot Extension Pack  
  스프링 부트 프로젝트 팔레트를 통해 간단하게 생성 가능.
  <br></br>
- Community Server Connectors  
  tomcat 익스텐션이 더이상 지원되지 않음에 따라 해당 익스텐션으로 대체.
  <br></br>
- Lombok
  Lombok 라이브러리(메서드 자동 완성 기능) 사용할 때 자동 완성 기능 제공.
  <br></br>

--------------------------------------

### 3. 스프링 부트 프로젝트 만들기

- vs 코드에서 Ctrl + shift + p 눌러 팔레트 실행.

- Spring initialzr: Create a Maven Project 입력

- 스프링 부트 버전 선택

- 프로젝트 언어 선택 (Java)

- Group Id 입력 (프로젝트 고유의 ID)

- Artifact Id 입력 (프로젝트 이름)

- packaging type 입력 (일반적으로 스프링부트는 Jar 타입 사용)

- 자바 버전 선택 (17 버전 선택)

- 의존성 설치
  Spring Boot DevTools, Lombok, Spirng Web

--------------------------------------

### 4. Gradle과 Maven의 차이

- 공통점 : 프로젝트를 빌드하고 관리하는 데에 사용되는 빌드 도구

- Maven
  - pom.xml을 사용하여 의존성 관리
  - 컨벤션 오버 구성: 프로젝트 구조와 설정 기본적으로 제공
  - 중앙 저장소를 통해 종속성을 관리해, 라이브러리를 간편하게 가져올 수 있음

- Gradle
  - 유연하고 강력한 빌드 스크립트, 사용자의 커스텀 용이
  - 구성 오버 컨벤션: 사용자가 빌드 스크립트를 자유롭게 작성하여, 프로젝트의 기능과 설정 세세하게 설정 가능
  - Maven과 호환 가능
 
- 정리
  - Maven은 초기 설정을 해줘서 뚝딱 만들어 내기가 쉽다.
  - Gradle은 사용자가 빌드를 커스텀해서 사용하기 좋다.

--------------------------------------

### 5. Jar, War의 차이

- 공통점 : Java 어플리케이션을 패키징 하기 위해 사용되는 파일 형식

- Jar
  - 라이브러리 형태로 패키징할 때 주로 사용, 다른 프로젝트에서 재사용할 수 있음
  - 압축된 zip 형식
  - 외부 자바 환경과 독립적
 
- War
  - 웹 어플리케이션을 구성하는 파일과 리소스 패키징할 때 사용
  - 웹 서버에 배포되어 실행
 
- 웹 어플리케이션을 만드는 스프링 부트에서 Jar 파일 형식을 사용하는 이유
  -  내장 서버를 사용하여 Jar 파일만 있더라도 실행이 가능함
  -  외부 자바 환경과 독립된 상태로 실행 가능
  -  배포와 실행이 간편
 
  -----------------------------------

### 6. 과정 진행 후 폴더 구조

  ```
📦board_springboot
 ┣ 📂.git
 ┃ ┣ 📂hooks
 ┃ ┃ ┣ 📜applypatch-msg.sample
 ┃ ┃ ┣ 📜commit-msg.sample
 ┃ ┃ ┣ 📜fsmonitor-watchman.sample
 ┃ ┃ ┣ 📜post-update.sample
 ┃ ┃ ┣ 📜pre-applypatch.sample
 ┃ ┃ ┣ 📜pre-commit.sample
 ┃ ┃ ┣ 📜pre-merge-commit.sample
 ┃ ┃ ┣ 📜pre-push.sample
 ┃ ┃ ┣ 📜pre-rebase.sample
 ┃ ┃ ┣ 📜pre-receive.sample
 ┃ ┃ ┣ 📜prepare-commit-msg.sample
 ┃ ┃ ┣ 📜push-to-checkout.sample
 ┃ ┃ ┗ 📜update.sample
 ┃ ┣ 📂info
 ┃ ┃ ┗ 📜exclude
 ┃ ┣ 📂logs
 ┃ ┃ ┣ 📂refs
 ┃ ┃ ┃ ┣ 📂heads
 ┃ ┃ ┃ ┃ ┣ 📜feat_use_jsp
 ┃ ┃ ┃ ┃ ┗ 📜master
 ┃ ┃ ┃ ┗ 📂remotes
 ┃ ┃ ┃ ┃ ┗ 📂origin
 ┃ ┃ ┃ ┃ ┃ ┣ 📜main
 ┃ ┃ ┃ ┃ ┃ ┗ 📜master
 ┃ ┃ ┗ 📜HEAD
 ┃ ┣ 📂objects
 ┃ ┃ ┣ 📂04
 ┃ ┃ ┃ ┗ 📜073b5c13c60e03502dcceb2683051838769aec
 ┃ ┃ ┣ 📂23
 ┃ ┃ ┃ ┗ 📜a5aaef75847431db41cfb3dff7ab2d2d84bf95
 ┃ ┃ ┣ 📂28
 ┃ ┃ ┃ ┣ 📜72d09106523e99758708b9b41370573d45580d
 ┃ ┃ ┃ ┗ 📜93f0eebb2ab6afdde7127add563e65273a22b0
 ┃ ┃ ┣ 📂29
 ┃ ┃ ┃ ┗ 📜dc0b6df613398bd97136fd75ad97be9c30b42e
 ┃ ┃ ┣ 📂36
 ┃ ┃ ┃ ┗ 📜dd59ea4d7f85950a515f75495b3c5986efddfe
 ┃ ┃ ┣ 📂45
 ┃ ┃ ┃ ┗ 📜be6aa4319413832f4be75df5849d40cebecde1
 ┃ ┃ ┣ 📂46
 ┃ ┃ ┃ ┣ 📜0ab5e5238638a9a1b69657dddf2280fa39d3c3
 ┃ ┃ ┃ ┣ 📜2686e25df6d2e44df43e1c8b42c45b7425372f
 ┃ ┃ ┃ ┗ 📜3e0729a4a448691aee1d12e2adea8460b8dd38
 ┃ ┃ ┣ 📂54
 ┃ ┃ ┃ ┗ 📜9e00a2a96fa9d7c5dbc9859664a78d980158c2
 ┃ ┃ ┣ 📂56
 ┃ ┃ ┃ ┗ 📜85e252b8c8d4e20ff16d80a3bd064c4392905e
 ┃ ┃ ┣ 📂5d
 ┃ ┃ ┃ ┗ 📜5e7e41ad9ecebf0c37b12930cc73c9ac8a5ad4
 ┃ ┃ ┣ 📂62
 ┃ ┃ ┃ ┗ 📜4b7fbe202d1bff24f0d6448af2685feb53e31c
 ┃ ┃ ┣ 📂64
 ┃ ┃ ┃ ┗ 📜47d76bdf1f7b4cbf4586435392d7390eaf70b4
 ┃ ┃ ┣ 📂66
 ┃ ┃ ┃ ┗ 📜df2854281f4cb6869e4830dd1a7abd1e946c18
 ┃ ┃ ┣ 📂69
 ┃ ┃ ┃ ┗ 📜1f67a66f1eae7b67a2d8110fad27698147b85f
 ┃ ┃ ┣ 📂6f
 ┃ ┃ ┃ ┗ 📜b43a90283d14535447a865c27d931c2e21b9af
 ┃ ┃ ┣ 📂87
 ┃ ┃ ┃ ┗ 📜6202aefa2d95fcf8468bc0c077c098c359181c
 ┃ ┃ ┣ 📂8b
 ┃ ┃ ┃ ┗ 📜137891791fe96927ad78e64b0aad7bded08bdc
 ┃ ┃ ┣ 📂95
 ┃ ┃ ┃ ┗ 📜ba6f54ac526de46248af840bab26f33f946b93
 ┃ ┃ ┣ 📂a0
 ┃ ┃ ┃ ┗ 📜db3cc996affe2a296aab5687d017a5147f1cf7
 ┃ ┃ ┣ 📂a6
 ┃ ┃ ┃ ┗ 📜f421a335df7b991128447f365c880f8128ff69
 ┃ ┃ ┣ 📂ac
 ┃ ┃ ┃ ┗ 📜b922f74f707c0b6044b8b42c1f9094a72a2747
 ┃ ┃ ┣ 📂b1
 ┃ ┃ ┃ ┗ 📜cd811da571435da6179c3242be4d9ff4b5a48f
 ┃ ┃ ┣ 📂b2
 ┃ ┃ ┃ ┗ 📜fc5f5a4e4d08135c11bedbb7055118426fde70
 ┃ ┃ ┣ 📂b3
 ┃ ┃ ┃ ┗ 📜1e20cd824258a08bf151dec0c6ee098125604c
 ┃ ┃ ┣ 📂cb
 ┃ ┃ ┃ ┗ 📜28b0e37c7d206feb564310fdeec0927af4123a
 ┃ ┃ ┣ 📂d9
 ┃ ┃ ┃ ┗ 📜6b787fc49ed3ab19cd11296b2f8ae0bcee99aa
 ┃ ┃ ┣ 📂de
 ┃ ┃ ┃ ┗ 📜e531c5607fd39c97425fde43372951a7a3eb4b
 ┃ ┃ ┣ 📂e9
 ┃ ┃ ┃ ┗ 📜baca95d3ea68fbafa28236e2c270faaa091cda
 ┃ ┃ ┣ 📂ee
 ┃ ┃ ┃ ┗ 📜ab22e3c57d2cb1e2a7a935de48f590cfbdf18a
 ┃ ┃ ┣ 📂ef
 ┃ ┃ ┃ ┗ 📜14ba3b749fc0e21a0c46da4f0523d4922ad933
 ┃ ┃ ┣ 📂f2
 ┃ ┃ ┃ ┗ 📜e452e584d07dee856dca4b12b78f86d4b5e8d1
 ┃ ┃ ┣ 📂info
 ┃ ┃ ┗ 📂pack
 ┃ ┃ ┃ ┣ 📜pack-09cd937162124a3d21fb6a48321a4b3c17e8aff5.idx
 ┃ ┃ ┃ ┗ 📜pack-09cd937162124a3d21fb6a48321a4b3c17e8aff5.pack
 ┃ ┣ 📂refs
 ┃ ┃ ┣ 📂heads
 ┃ ┃ ┃ ┣ 📜feat_use_jsp
 ┃ ┃ ┃ ┗ 📜master
 ┃ ┃ ┣ 📂remotes
 ┃ ┃ ┃ ┗ 📂origin
 ┃ ┃ ┃ ┃ ┣ 📜main
 ┃ ┃ ┃ ┃ ┗ 📜master
 ┃ ┃ ┗ 📂tags
 ┃ ┣ 📜COMMIT_EDITMSG
 ┃ ┣ 📜config
 ┃ ┣ 📜description
 ┃ ┣ 📜FETCH_HEAD
 ┃ ┣ 📜HEAD
 ┃ ┣ 📜index
 ┃ ┗ 📜ORIG_HEAD
 ┣ 📂.github
 ┃ ┣ 📂ISSUE_TEMPLATE
 ┃ ┃ ┗ 📜문제-기록.md
 ┃ ┗ 📜.gitmessage.txt
 ┣ 📂.mvn
 ┃ ┗ 📂wrapper
 ┃ ┃ ┣ 📜maven-wrapper.jar
 ┃ ┃ ┗ 📜maven-wrapper.properties
 ┣ 📂.vscode
 ┃ ┗ 📜setting.json
 ┣ 📂src
 ┃ ┣ 📂main
 ┃ ┃ ┣ 📂java
 ┃ ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┃ ┗ 📂example
 ┃ ┃ ┃ ┃ ┃ ┗ 📂board_springboot
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardSpringbootApplication.java
 ┃ ┃ ┗ 📂resources
 ┃ ┃ ┃ ┣ 📂static
 ┃ ┃ ┃ ┣ 📂templates
 ┃ ┃ ┃ ┗ 📜application.properties
 ┃ ┗ 📂test
 ┃ ┃ ┗ 📂java
 ┃ ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┃ ┗ 📂example
 ┃ ┃ ┃ ┃ ┃ ┗ 📂board_springboot
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardSpringbootApplicationTests.java
 ┣ 📂target
 ┃ ┣ 📂classes
 ┃ ┃ ┣ 📂com
 ┃ ┃ ┃ ┗ 📂example
 ┃ ┃ ┃ ┃ ┗ 📂board_springboot
 ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardSpringbootApplication.class
 ┃ ┃ ┗ 📜application.properties
 ┃ ┣ 📂generated-sources
 ┃ ┃ ┗ 📂annotations
 ┃ ┣ 📂generated-test-sources
 ┃ ┃ ┗ 📂test-annotations
 ┃ ┗ 📂test-classes
 ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┗ 📂example
 ┃ ┃ ┃ ┃ ┗ 📂board_springboot
 ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardSpringbootApplicationTests.class
 ┣ 📜.gitignore
 ┣ 📜HELP.md
 ┣ 📜mvnw
 ┣ 📜mvnw.cmd
 ┣ 📜pom.xml
 ┗ 📜README.md
  ```
